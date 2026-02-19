# Entitlements

## Overview

An `Entitlement` grants a customer the right to access and use a specific product feature.

### Available Operations

* [listActive](#listactive) - List by Customer
* [create](#create) - Create
* [list](#list) - List Entitlements

## listActive

List by Customer

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getActiveEntitlements" method="get" path="/v0/entitlements/activeEntitlements" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.listActive({
    customerId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsListActive } from "@paygentic/sdk/funcs/entitlementsListActive.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsListActive(paygentic, {
    customerId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsListActive failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetActiveEntitlementsRequest](../../models/operations/getactiveentitlementsrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetActiveEntitlementsResponse](../../models/operations/getactiveentitlementsresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403                          | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## create

Create an entitlement for a customer. This temporarily reserves funds in the customer's wallet to guarantee payment for future usage.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="createEntitlement" method="post" path="/v0/entitlements" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.create({
    customerId: "<id>",
    entitlementData: [],
    merchantId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsCreate } from "@paygentic/sdk/funcs/entitlementsCreate.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsCreate(paygentic, {
    customerId: "<id>",
    entitlementData: [],
    merchantId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.CreateEntitlementRequest](../../models/createentitlementrequest.md)                                                                                                    | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.Entitlement](../../models/entitlement.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403                          | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## list

Retrieve all entitlements for a customer, optionally filtered by feature or product.

### Example Usage: emptyResult

<!-- UsageSnippet language="typescript" operationID="listEntitlements" method="get" path="/v1/entitlements" example="emptyResult" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.list({
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsList } from "@paygentic/sdk/funcs/entitlementsList.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsList(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsList failed:", res.error);
  }
}

run();
```
### Example Usage: expiredEntitlement

<!-- UsageSnippet language="typescript" operationID="listEntitlements" method="get" path="/v1/entitlements" example="expiredEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.list({
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsList } from "@paygentic/sdk/funcs/entitlementsList.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsList(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsList failed:", res.error);
  }
}

run();
```
### Example Usage: multipleEntitlements

<!-- UsageSnippet language="typescript" operationID="listEntitlements" method="get" path="/v1/entitlements" example="multipleEntitlements" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.list({
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsList } from "@paygentic/sdk/funcs/entitlementsList.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsList(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsList failed:", res.error);
  }
}

run();
```
### Example Usage: staticFeatureWithConfig

<!-- UsageSnippet language="typescript" operationID="listEntitlements" method="get" path="/v1/entitlements" example="staticFeatureWithConfig" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.list({
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsList } from "@paygentic/sdk/funcs/entitlementsList.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsList(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsList failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ListEntitlementsRequest](../../models/operations/listentitlementsrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ListEntitlementsResponse](../../models/operations/listentitlementsresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403                          | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |