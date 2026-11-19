# SubscriptionProposals

## Overview

A `SubscriptionProposal` holds the values of a subscription until a person on your team approves or rejects it. Nothing is billed while it waits.

### Available Operations

* [listSubscriptionProposals](#listsubscriptionproposals) - List
* [createSubscriptionProposal](#createsubscriptionproposal) - Create
* [getSubscriptionProposal](#getsubscriptionproposal) - Get
* [updateSubscriptionProposal](#updatesubscriptionproposal) - Amend
* [decideSubscriptionProposal](#decidesubscriptionproposal) - Approve or reject
* [listSubscriptionProposalProjectedInvoices](#listsubscriptionproposalprojectedinvoices) - List projected

## listSubscriptionProposals

Lists the subscription proposals you can read, newest first. Filter by `status` to list, for example, the proposals waiting for a decision: `pagination.total` then counts them. Pass `merchantId` to list one merchant's proposals. A `merchantId` you cannot read answers 403, not an empty page.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSubscriptionProposals" method="get" path="/v0/subscriptionProposals" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.listSubscriptionProposals({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsListSubscriptionProposals } from "@paygentic/sdk/funcs/subscriptionProposalsListSubscriptionProposals.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsListSubscriptionProposals(paygentic, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsListSubscriptionProposals failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSubscriptionProposalsRequest](../../models/operations/listsubscriptionproposalsrequest.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSubscriptionProposalsResponse](../../models/operations/listsubscriptionproposalsresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## createSubscriptionProposal

Creates a pending subscription proposal from the values of a subscription create. The customer must already exist. A plan or customer of another merchant answers 404, as an unknown one does. The values are checked as subscription create checks them, at the moment of the request, but no subscription, invoice or entitlement exists until a person approves the proposal.

With an `externalReference`, the create first finds the proposal that record already has: its pending or approved proposal, else its most recent rejected one. Sends of one record are handled one at a time. Values are compared after normalization: key order does not count, a field sent with its default equals the field left out, and two forms of one instant, such as `Z` and `+00:00`, are equal.

- None found: a new proposal, 201.
- Values equal to that proposal's `requested`: the proposal, 200. Nothing is checked. A stored `refusedResync` is cleared, which raises `lockVersion` and changes `hash`; without one, nothing is written.
- A pending proposal, values changed: the values become the next revision and `requested`. `current` takes each changed field except a field in `amendedFields`, which keeps the person's value, and a field left out returns to its default. The result is checked as an amend is, and answered 200.
- A pending proposal whose change conflicts with an amendment: 409 `SUBSCRIPTION_PROPOSAL_RESYNC_CONFLICT`, and `current` and `requested` do not change. `details.fields` names each conflicting field. A field conflicts when the client changed it, a person amended it, and the new value differs from `current`. Leaving out a field the previous send set changes it to its default, so leaving out an amended field conflicts too. A change also conflicts when it would leave price fields (`planVersionId`, `overridePrices`, `addPrices`, `removePrices`, `adjustments`) naming another plan's prices, and when it would change `versionPolicy` while `planVersionId` is amended.
- An approved proposal, values changed: 409 `SUBSCRIPTION_PROPOSAL_ALREADY_APPROVED`, with the subscription's id in `details.subscriptionId`. Changes to an active subscription are not supported yet.
- A rejected proposal, values changed: a new proposal, 201. The rejected one is unchanged.

A refused send is kept on the proposal as `refusedResync`, so a reviewer sees it. A send that repeats the stored refusal changes nothing.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createSubscriptionProposal" method="post" path="/v0/subscriptionProposals" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.createSubscriptionProposal({
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    startedAt: new Date("2024-06-17T10:38:54.507Z"),
    adjustments: [
      {
        type: "percentageDiscount",
        percentageDiscount: "<value>",
        effectiveFrom: new Date("2026-04-27T04:00:33.243Z"),
      },
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsCreateSubscriptionProposal } from "@paygentic/sdk/funcs/subscriptionProposalsCreateSubscriptionProposal.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsCreateSubscriptionProposal(paygentic, {
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    startedAt: new Date("2024-06-17T10:38:54.507Z"),
    adjustments: [
      {
        type: "percentageDiscount",
        percentageDiscount: "<value>",
        effectiveFrom: new Date("2026-04-27T04:00:33.243Z"),
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsCreateSubscriptionProposal failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateSubscriptionProposalRequest](../../models/operations/createsubscriptionproposalrequest.md)                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SubscriptionProposal](../../models/subscriptionproposal.md)\>**

### Errors

| Error Type                               | Status Code                              | Content Type                             |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| errors.ErrorT                            | 400                                      | application/json                         |
| errors.ValidationError                   | 400                                      | application/json                         |
| errors.SubscriptionProposalConflictError | 409                                      | application/json                         |
| errors.ErrorT                            | 401, 403, 404, 429                       | application/json                         |
| errors.ErrorT                            | 500                                      | application/json                         |
| errors.PaygenticDefaultError             | 4XX, 5XX                                 | \*/\*                                    |

## getSubscriptionProposal

Returns one subscription proposal. Pass `expand=revisions` to add each set of values its client sent, earliest first. A proposal of another merchant answers 404, as an unknown one does.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getSubscriptionProposal" method="get" path="/v0/subscriptionProposals/{id}" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.getSubscriptionProposal({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsGetSubscriptionProposal } from "@paygentic/sdk/funcs/subscriptionProposalsGetSubscriptionProposal.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsGetSubscriptionProposal(paygentic, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsGetSubscriptionProposal failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetSubscriptionProposalRequest](../../models/operations/getsubscriptionproposalrequest.md)                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SubscriptionProposal](../../models/subscriptionproposal.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403, 404                | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## updateSubscriptionProposal

Changes the values of a pending subscription proposal before it is decided. Send only the fields to change. `requested`, the values the source sent, stays as it is, and `current` takes the changes. A field sent with a value other than its `requested` value joins `amendedFields`, a field sent with its `requested` value leaves it, and a field not sent keeps its state. Only a pinned proposal names a version. Its `planVersionId` compares with the version a `pinned` `requested` names, else with the plan's default version; on a proposal the source sent floating, a pinned version is amended.

Set a nullable field to null to clear it: the field leaves `current`, and the default a create applies takes its place. On a pinned proposal, `planVersionId: null`, or a new `planId` without a `planVersionId`, pins the plan's default version. Setting `versionPolicy` to `floating` drops the version: the proposal then follows the plan's default. `elapsedPeriodBilling`, `versionPolicy`, `metadata`, `changeReason` and `changeMetadata` take no null: to reset one, send its default value (`none`, `floating`, `{}`, `unspecified` and `{}`).

The result is checked as a subscription create checks its values, at the moment of the request, and a request that fails a check changes nothing. A request that changes neither `current` nor `amendedFields` is not checked: it writes nothing and answers the proposal as it is, even when the proposal has become invalid since its last change, for example past the twelve-month limit of `per_period`. A plan or plan version that no longer exists still answers 404. A proposal that is no longer pending answers 409 with the code `SUBSCRIPTION_PROPOSAL_NOT_PENDING`. With `basedOnHash`, a proposal whose `hash` changed since it was read answers 409 `SUBSCRIPTION_PROPOSAL_CHANGED`, after the pending check, so two reviewers cannot overwrite each other's amends. A proposal of another merchant answers 404, as an unknown one does.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="updateSubscriptionProposal" method="patch" path="/v0/subscriptionProposals/{id}" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.updateSubscriptionProposal({
    id: "<id>",
    requestBody: {
      adjustments: [
        {
          type: "maximumQuantity",
          maximumQuantity: "<value>",
          targetPriceIds: [
            "<value 1>",
            "<value 2>",
          ],
          effectiveFrom: new Date("2024-07-04T21:55:42.464Z"),
        },
      ],
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsUpdateSubscriptionProposal } from "@paygentic/sdk/funcs/subscriptionProposalsUpdateSubscriptionProposal.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsUpdateSubscriptionProposal(paygentic, {
    id: "<id>",
    requestBody: {
      adjustments: [
        {
          type: "maximumQuantity",
          maximumQuantity: "<value>",
          targetPriceIds: [
            "<value 1>",
            "<value 2>",
          ],
          effectiveFrom: new Date("2024-07-04T21:55:42.464Z"),
        },
      ],
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsUpdateSubscriptionProposal failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.UpdateSubscriptionProposalRequest](../../models/operations/updatesubscriptionproposalrequest.md)                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SubscriptionProposal](../../models/subscriptionproposal.md)\>**

### Errors

| Error Type                               | Status Code                              | Content Type                             |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| errors.ErrorT                            | 400                                      | application/json                         |
| errors.ValidationError                   | 400                                      | application/json                         |
| errors.SubscriptionProposalConflictError | 409                                      | application/json                         |
| errors.ErrorT                            | 401, 403, 404, 429                       | application/json                         |
| errors.ErrorT                            | 500                                      | application/json                         |
| errors.PaygenticDefaultError             | 4XX, 5XX                                 | \*/\*                                    |

## decideSubscriptionProposal

Approves or rejects a pending subscription proposal. The body is flat like `PATCH /v0/approvals/{id}`'s, but takes the verbs `approve` and `reject`, a `reason` from a fixed list with optional `text`, and no `cancelled`. Needs the `subscriptionProposals:approve` permission, whoever created the proposal. Send the proposal's `hash` as `basedOnHash`. `approve` creates the subscription that `POST /v0/subscriptions` would create from the proposal's values at the moment of approval, read from the proposal's test clock when it has one, on its pinned version or, for a floating proposal, on the plan's default at that moment. The proposal becomes `approved` with the new `subscriptionId` in the same transaction. The answer comes once the first invoice is raised, as subscription create's does; read the subscription, with its payment state, from `GET /v0/subscriptions/{id}`. An approval takes no `reason` or `text`. An `approve` of an `approved` proposal whose `strandedAt` is set resumes the subscription its approval left waiting for its first invoice, and answers `SUBSCRIPTION_PROPOSAL_CHANGED` when another approve claimed it after this one read it. `reject` records the reason, the text, who decided and when. The proposal becomes `rejected`, which is final. No subscription is created, and nothing is sent to the system the proposal came from. 409 carries a `code`: `SUBSCRIPTION_PROPOSAL_NOT_PENDING` for a proposal that is not `pending`; `SUBSCRIPTION_PROPOSAL_CHANGED` when its `hash` changed since it was read, by an amend or a new default of a floating proposal's plan, or when it changed while the approval ran, with `details` `{ field: 'lockVersion', expected, actual }`; `SUBSCRIPTION_PROPOSAL_INVALID` when approving finds the proposal fails a check subscription create makes, with `details.code` the failed check's own code and `details.details` its details, each only when the check has one; `SUBSCRIPTION_PROPOSAL_DUPLICATE` when the customer already has a live subscription for the plan's product; `SUBSCRIPTION_PROPOSAL_ALREADY_APPROVED` when that subscription is the one a concurrent approval of this proposal created. Both put the subscription's id in `details.subscriptionId`. On any 409 the proposal is left as it is, except that an `approve` of a proposal whose `strandedAt` is set, when its subscription is no longer waiting for its first invoice, clears `strandedAt` and answers `SUBSCRIPTION_PROPOSAL_NOT_PENDING`. A plan, plan version or customer that no longer exists answers 404. A pending proposal blocks deleting its plan and its customer, so this happens only when a delete runs at the same time. A proposal of another merchant answers 404, as an unknown one does.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="decideSubscriptionProposal" method="post" path="/v0/subscriptionProposals/{id}/decision" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.decideSubscriptionProposal({
    id: "<id>",
    subscriptionProposalDecision: {
      decision: "approve",
      basedOnHash: "<value>",
    },
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsDecideSubscriptionProposal } from "@paygentic/sdk/funcs/subscriptionProposalsDecideSubscriptionProposal.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsDecideSubscriptionProposal(paygentic, {
    id: "<id>",
    subscriptionProposalDecision: {
      decision: "approve",
      basedOnHash: "<value>",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsDecideSubscriptionProposal failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.DecideSubscriptionProposalRequest](../../models/operations/decidesubscriptionproposalrequest.md)                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.SubscriptionProposal](../../models/subscriptionproposal.md)\>**

### Errors

| Error Type                               | Status Code                              | Content Type                             |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| errors.ErrorT                            | 400                                      | application/json                         |
| errors.ValidationError                   | 400                                      | application/json                         |
| errors.SubscriptionProposalConflictError | 409                                      | application/json                         |
| errors.ErrorT                            | 401, 403, 404, 429                       | application/json                         |
| errors.ErrorT                            | 500                                      | application/json                         |
| errors.PaygenticDefaultError             | 4XX, 5XX                                 | \*/\*                                    |

## listSubscriptionProposalProjectedInvoices

Returns the invoices that approving this pending subscription proposal now would raise, as a list of `Invoice` in the envelope `GET /v2/invoices/projected` answers. It is not that endpoint: it takes no `from` or `to`, and it prices an elapsed metered period as described below. Today `data` holds the first invoice only, with the lines and amounts approve would bill at the moment of this read, and it is empty when approving now would raise no invoice. `pagination.total` says whether anything is owed: 1 when it is and 0 when it is not, whatever the offset. Nothing is stored, and the content is as of this read: the clock, the plan, its prices and the customer can change it before approval. The tax and the total are estimates from stored tax rates, not the tax provider's calculation. Grant discounts are not applied. A metered period that has already elapsed shows at zero usage, or at a minimum quantity in force for that period. `subscriptionId` holds the proposal id, because no subscription exists yet, so `GET /v0/subscriptions/{id}` answers 404 for it. The invoice has status `PROJECTED` and an id that is the same on every read, but `GET /v2/invoices/{id}` answers 404 for it. Needs the `subscriptionProposals:read` permission. The preview refuses what approve would refuse, with approve's answer. A plan, plan version or customer that no longer exists answers 404. A pending proposal blocks deleting its plan and its customer, so this happens only when a delete runs at the same time. A proposal of another merchant answers 404, as an unknown one does. 409 carries a `code`: `SUBSCRIPTION_PROPOSAL_NOT_PENDING` for a proposal that is not `pending`; `SUBSCRIPTION_PROPOSAL_INVALID` when the proposal fails a check subscription create makes, with `details.code` the failed check's own code and `details.details` its details, each only when the check has one; `SUBSCRIPTION_PROPOSAL_DUPLICATE` when the customer already has a live subscription for the plan's product, with its id in `details.subscriptionId`.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listSubscriptionProposalProjectedInvoices" method="get" path="/v0/subscriptionProposals/{id}/projected" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.subscriptionProposals.listSubscriptionProposalProjectedInvoices({
    id: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { subscriptionProposalsListSubscriptionProposalProjectedInvoices } from "@paygentic/sdk/funcs/subscriptionProposalsListSubscriptionProposalProjectedInvoices.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await subscriptionProposalsListSubscriptionProposalProjectedInvoices(paygentic, {
    id: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("subscriptionProposalsListSubscriptionProposalProjectedInvoices failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListSubscriptionProposalProjectedInvoicesRequest](../../models/operations/listsubscriptionproposalprojectedinvoicesrequest.md)                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListSubscriptionProposalProjectedInvoicesResponse](../../models/operations/listsubscriptionproposalprojectedinvoicesresponse.md)\>**

### Errors

| Error Type                               | Status Code                              | Content Type                             |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| errors.ErrorT                            | 400                                      | application/json                         |
| errors.ValidationError                   | 400                                      | application/json                         |
| errors.SubscriptionProposalConflictError | 409                                      | application/json                         |
| errors.ErrorT                            | 401, 403, 404, 429                       | application/json                         |
| errors.ErrorT                            | 500                                      | application/json                         |
| errors.PaygenticDefaultError             | 4XX, 5XX                                 | \*/\*                                    |