# SubscriptionProposal

A subscription a client proposed, held until a person approves or rejects it. No subscription exists until it is approved.

## Example Usage

```typescript
import { SubscriptionProposal } from "@paygentic/sdk/models";

let value: SubscriptionProposal = {
  id: "<id>",
  object: "subscriptionProposal",
  merchantId: "<id>",
  status: "approved",
  customerId: "<id>",
  planId: "<id>",
  planVersionId: "<id>",
  resolvedPlanVersionId: "<id>",
  hash: "<value>",
  testClockId: "<id>",
  requested: {
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    startedAt: new Date("2024-09-21T16:04:12.116Z"),
    adjustments: [
      {
        type: "percentageDiscount",
        percentageDiscount: "<value>",
        effectiveFrom: new Date("2024-08-07T07:27:16.428Z"),
      },
    ],
  },
  current: {
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    startedAt: new Date("2026-02-02T17:43:02.474Z"),
    adjustments: [
      {
        type: "minimumQuantity",
        minimumQuantity: "<value>",
        targetPriceIds: [],
        effectiveFrom: new Date("2025-08-21T02:50:02.552Z"),
      },
    ],
  },
  amendedFields: [
    "<value 1>",
    "<value 2>",
  ],
  refusedResync: {
    receivedAt: new Date("2026-09-08T02:08:38.336Z"),
    code: "SUBSCRIPTION_PROPOSAL_RESYNC_CONFLICT",
    fields: [
      "<value 1>",
    ],
    values: {
      customerId: "<id>",
      name: "<value>",
      planId: "<id>",
      startedAt: new Date("2025-06-24T21:11:03.224Z"),
      adjustments: [
        {
          type: "maximumQuantity",
          maximumQuantity: "<value>",
          targetPriceIds: [],
          effectiveFrom: new Date("2024-04-27T21:00:10.696Z"),
        },
      ],
    },
    credentialId: "<id>",
  },
  lockVersion: 459814,
  source: "<value>",
  externalReference: {
    provider: "<value>",
    externalId: "<id>",
  },
  subscriptionId: "<id>",
  rejectionReason: "price_mismatch",
  rejectionText: "<value>",
  decidedAt: new Date("2026-07-05T19:20:37.099Z"),
  decidedByPrincipalId: "<id>",
  decidedBy: null,
  strandedAt: new Date("2024-04-03T18:55:00.514Z"),
  createdByPrincipalId: "<id>",
  createdByCredentialId: "<id>",
  createdAt: new Date("2024-06-26T21:52:10.542Z"),
  updatedAt: new Date("2026-05-26T03:35:44.317Z"),
  revisions: [
    {
      id: "<id>",
      version: 944829,
      values: {
        customerId: "<id>",
        name: "<value>",
        planId: "<id>",
        startedAt: new Date("2025-06-24T21:11:03.224Z"),
        adjustments: [
          {
            type: "maximumQuantity",
            maximumQuantity: "<value>",
            targetPriceIds: [],
            effectiveFrom: new Date("2024-04-27T21:00:10.696Z"),
          },
        ],
      },
      createdAt: new Date("2024-10-16T21:19:26.722Z"),
      createdByCredentialId: "<id>",
    },
  ],
};
```

## Fields

| Field                                                                                                                                                                                           | Type                                                                                                                                                                                            | Required                                                                                                                                                                                        | Description                                                                                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                                                                                            | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `object`                                                                                                                                                                                        | [models.SubscriptionProposalObject](../models/subscriptionproposalobject.md)                                                                                                                    | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `merchantId`                                                                                                                                                                                    | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | Unique identifier for an organization                                                                                                                                                           |
| `status`                                                                                                                                                                                        | [models.SubscriptionProposalStatus](../models/subscriptionproposalstatus.md)                                                                                                                    | :heavy_check_mark:                                                                                                                                                                              | `pending` until a person approves or rejects the proposal.                                                                                                                                      |
| `customerId`                                                                                                                                                                                    | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | Unique identifier for a customer                                                                                                                                                                |
| `planId`                                                                                                                                                                                        | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | Unique identifier for a plan                                                                                                                                                                    |
| `planVersionId`                                                                                                                                                                                 | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The plan version a pinned proposal is pinned to. Null for a floating proposal, which follows the plan's default version.                                                                        |
| `resolvedPlanVersionId`                                                                                                                                                                         | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The plan version approve would use now: `planVersionId` when pinned, else the plan's default version. Null when the plan has no published version.                                              |
| `hash`                                                                                                                                                                                          | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | Changes whenever `current` or `resolvedPlanVersionId` changes. A decision sends it as `basedOnHash`, so a person only decides on the proposal they read.                                        |
| `testClockId`                                                                                                                                                                                   | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `requested`                                                                                                                                                                                     | [models.SubscriptionProposalValues](../models/subscriptionproposalvalues.md)                                                                                                                    | :heavy_check_mark:                                                                                                                                                                              | The values of a subscription proposal: the fields of `POST /v0/subscriptionProposals` without `externalReference`, each as that request takes it. A field the client left out is absent.        |
| `current`                                                                                                                                                                                       | [models.SubscriptionProposalValues](../models/subscriptionproposalvalues.md)                                                                                                                    | :heavy_check_mark:                                                                                                                                                                              | The values of a subscription proposal: the fields of `POST /v0/subscriptionProposals` without `externalReference`, each as that request takes it. A field the client left out is absent.        |
| `amendedFields`                                                                                                                                                                                 | *string*[]                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                              | The top-level fields a person amended. A re-send of the external reference keeps the person's value for each; a field stays amended when the client sends the person's value.                   |
| `refusedResync`                                                                                                                                                                                 | [models.SubscriptionProposalRefusedResync](../models/subscriptionproposalrefusedresync.md)                                                                                                      | :heavy_check_mark:                                                                                                                                                                              | The CRM's latest refused re-sync, or null. It changes `hash`, so a decision made before it arrived answers 409 `SUBSCRIPTION_PROPOSAL_CHANGED`.                                                 |
| `lockVersion`                                                                                                                                                                                   | *number*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | Starts at 1, and every change to the proposal adds one.                                                                                                                                         |
| `source`                                                                                                                                                                                        | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The `provider` of the proposal's external reference, or `api` when it has none.                                                                                                                 |
| `externalReference`                                                                                                                                                                             | [models.SubscriptionProposalExternalReference](../models/subscriptionproposalexternalreference.md)                                                                                              | :heavy_check_mark:                                                                                                                                                                              | The record the proposal comes from. Null when it was created without one.                                                                                                                       |
| `subscriptionId`                                                                                                                                                                                | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The subscription approve created.                                                                                                                                                               |
| `rejectionReason`                                                                                                                                                                               | [models.SubscriptionProposalRejectionReason](../models/subscriptionproposalrejectionreason.md)                                                                                                  | :heavy_check_mark:                                                                                                                                                                              | Why the proposal was rejected. Null unless it is `rejected`.                                                                                                                                    |
| `rejectionText`                                                                                                                                                                                 | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The notes the reviewer gave with the rejection.                                                                                                                                                 |
| `decidedAt`                                                                                                                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                   | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `decidedByPrincipalId`                                                                                                                                                                          | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `decidedBy`                                                                                                                                                                                     | [models.SubscriptionProposalDecider](../models/subscriptionproposaldecider.md)                                                                                                                  | :heavy_check_mark:                                                                                                                                                                              | Who approved or rejected the proposal, by name. Null until it is decided, and when the decider cannot be named: a decision made with the platform key, or by a principal that no longer exists. |
| `strandedAt`                                                                                                                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                   | :heavy_check_mark:                                                                                                                                                                              | Set when an approve ended with its subscription waiting for its first invoice; a repeated approve resumes it.                                                                                   |
| `createdByPrincipalId`                                                                                                                                                                          | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `createdByCredentialId`                                                                                                                                                                         | *string*                                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                              | The API key or OAuth client that created the proposal; null for a dashboard session.                                                                                                            |
| `createdAt`                                                                                                                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                   | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `updatedAt`                                                                                                                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                                   | :heavy_check_mark:                                                                                                                                                                              | N/A                                                                                                                                                                                             |
| `revisions`                                                                                                                                                                                     | [models.SubscriptionProposalRevision](../models/subscriptionproposalrevision.md)[]                                                                                                              | :heavy_minus_sign:                                                                                                                                                                              | Each set of values the client sent, earliest first. Present only with `expand=revisions`. The last one is `requested`.                                                                          |