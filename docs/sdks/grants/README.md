# Entitlements.Grants

## Overview

### Available Operations

* [list](#list) - List Grants
* [create](#create) - Create Grant
* [purchase](#purchase) - Purchase Grant
* [get](#get) - Get Grant
* [void](#void) - Void Grant

## list

List grants for a metered entitlement. Active grants are returned by default; pass `includeVoided=true` to include voided grants.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="listEntitlementGrants" method="get" path="/v1/entitlements/{entitlementId}/grants" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.list({
    entitlementId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsGrantsList } from "@paygentic/sdk/funcs/entitlementsGrantsList.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsList(paygentic, {
    entitlementId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListEntitlementGrantsRequest](../../models/operations/listentitlementgrantsrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListEntitlementGrantsResponse](../../models/operations/listentitlementgrantsresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## create

Create a grant directly for a metered entitlement, crediting the customer's balance immediately. The entitlement must belong to an active v1 subscription.

### Example Usage: minimal

<!-- UsageSnippet language="typescript" operationID="createEntitlementGrant" method="post" path="/v1/entitlements/{entitlementId}/grants" example="minimal" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.create({
    entitlementId: "<id>",
    createGrantRequest: {
      amount: 100,
      idempotencyKey: "grant-initial-100",
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
import { entitlementsGrantsCreate } from "@paygentic/sdk/funcs/entitlementsGrantsCreate.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsCreate(paygentic, {
    entitlementId: "<id>",
    createGrantRequest: {
      amount: 100,
      idempotencyKey: "grant-initial-100",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsCreate failed:", res.error);
  }
}

run();
```
### Example Usage: withExpiry

<!-- UsageSnippet language="typescript" operationID="createEntitlementGrant" method="post" path="/v1/entitlements/{entitlementId}/grants" example="withExpiry" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.create({
    entitlementId: "<id>",
    createGrantRequest: {
      amount: 500,
      effectiveAt: new Date("2026-03-14T00:00:00Z"),
      expiresAt: new Date("2026-04-14T00:00:00Z"),
      idempotencyKey: "grant-march-2026-promo",
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
import { entitlementsGrantsCreate } from "@paygentic/sdk/funcs/entitlementsGrantsCreate.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsCreate(paygentic, {
    entitlementId: "<id>",
    createGrantRequest: {
      amount: 500,
      effectiveAt: new Date("2026-03-14T00:00:00Z"),
      expiresAt: new Date("2026-04-14T00:00:00Z"),
      idempotencyKey: "grant-march-2026-promo",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.CreateEntitlementGrantRequest](../../models/operations/createentitlementgrantrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Grant](../../models/grant.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404, 409                | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## purchase

Create an ad-hoc invoice with a payment session for a grant purchase. The customer pays via the returned payment URL; the grant is created automatically on payment completion. If payment expires, the invoice is cancelled and no grant is created.

After the consumer completes payment, the grant is created automatically. To confirm payment completion, poll `GET /v2/invoices/{invoiceId}` using the `invoiceId` from the response and check for `status === "PAID"`. Recommended polling interval: 2 seconds, timeout: 60 seconds.

### Example Usage: basic

<!-- UsageSnippet language="typescript" operationID="purchaseEntitlementGrant" method="post" path="/v1/entitlements/{entitlementId}/grants/purchase" example="basic" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.purchase({
    entitlementId: "<id>",
    purchaseGrantRequest: {
      amount: 1000,
      price: "5.00",
      idempotencyKey: "purchase-march-2026-topup",
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
import { entitlementsGrantsPurchase } from "@paygentic/sdk/funcs/entitlementsGrantsPurchase.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsPurchase(paygentic, {
    entitlementId: "<id>",
    purchaseGrantRequest: {
      amount: 1000,
      price: "5.00",
      idempotencyKey: "purchase-march-2026-topup",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsPurchase failed:", res.error);
  }
}

run();
```
### Example Usage: withOptions

<!-- UsageSnippet language="typescript" operationID="purchaseEntitlementGrant" method="post" path="/v1/entitlements/{entitlementId}/grants/purchase" example="withOptions" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.purchase({
    entitlementId: "<id>",
    purchaseGrantRequest: {
      amount: 500,
      price: "2.50",
      idempotencyKey: "purchase-promo-500",
      effectiveAt: new Date("2026-03-14T00:00:00Z"),
      expiresAt: new Date("2026-04-14T00:00:00Z"),
      successUrl: "https://example.com/success",
      cancelUrl: "https://example.com/cancel",
      paymentExpiresAt: new Date("2026-03-15T00:00:00Z"),
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
import { entitlementsGrantsPurchase } from "@paygentic/sdk/funcs/entitlementsGrantsPurchase.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsPurchase(paygentic, {
    entitlementId: "<id>",
    purchaseGrantRequest: {
      amount: 500,
      price: "2.50",
      idempotencyKey: "purchase-promo-500",
      effectiveAt: new Date("2026-03-14T00:00:00Z"),
      expiresAt: new Date("2026-04-14T00:00:00Z"),
      successUrl: "https://example.com/success",
      cancelUrl: "https://example.com/cancel",
      paymentExpiresAt: new Date("2026-03-15T00:00:00Z"),
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsPurchase failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PurchaseEntitlementGrantRequest](../../models/operations/purchaseentitlementgrantrequest.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.PurchaseGrantResponse](../../models/purchasegrantresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404, 409                | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## get

Retrieve a specific grant by ID.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getEntitlementGrant" method="get" path="/v1/entitlements/{entitlementId}/grants/{grantId}" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.get({
    entitlementId: "<id>",
    grantId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsGrantsGet } from "@paygentic/sdk/funcs/entitlementsGrantsGet.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsGet(paygentic, {
    entitlementId: "<id>",
    grantId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetEntitlementGrantRequest](../../models/operations/getentitlementgrantrequest.md)                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Grant](../../models/grant.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## void

Void a grant, removing it from the customer's balance. This operation is idempotent — voiding an already-voided grant returns the voided grant without error.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="voidEntitlementGrant" method="delete" path="/v1/entitlements/{entitlementId}/grants/{grantId}" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.grants.void({
    entitlementId: "<id>",
    grantId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsGrantsVoid } from "@paygentic/sdk/funcs/entitlementsGrantsVoid.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGrantsVoid(paygentic, {
    entitlementId: "<id>",
    grantId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGrantsVoid failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.VoidEntitlementGrantRequest](../../models/operations/voidentitlementgrantrequest.md)                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Grant](../../models/grant.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |