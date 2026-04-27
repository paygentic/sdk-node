# Entitlements

## Overview

### Available Operations

* [list](#list) - List Entitlements
* [issue](#issue) - Issue Entitlement
* [get](#get) - Get Entitlement

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

## issue

Issue a new entitlement to a customer, granting them access to a specific feature. The feature must exist and belong to the same merchant as the customer.

### Example Usage: booleanEntitlement

<!-- UsageSnippet language="typescript" operationID="issueEntitlement" method="post" path="/v1/entitlements" example="booleanEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.issue({
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "boolean",
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
import { entitlementsIssue } from "@paygentic/sdk/funcs/entitlementsIssue.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsIssue(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "boolean",
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsIssue failed:", res.error);
  }
}

run();
```
### Example Usage: staticEntitlement

<!-- UsageSnippet language="typescript" operationID="issueEntitlement" method="post" path="/v1/entitlements" example="staticEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.issue({
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "static",
      config: {
        "limit": 25,
        "tier": "pro",
      },
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
import { entitlementsIssue } from "@paygentic/sdk/funcs/entitlementsIssue.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsIssue(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "static",
      config: {
        "limit": 25,
        "tier": "pro",
      },
    },
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsIssue failed:", res.error);
  }
}

run();
```
### Example Usage: timedEntitlement

<!-- UsageSnippet language="typescript" operationID="issueEntitlement" method="post" path="/v1/entitlements" example="timedEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.issue({
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "boolean",
    },
    activeFrom: new Date("2024-01-01T00:00:00Z"),
    activeTo: new Date("2025-01-01T00:00:00Z"),
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { entitlementsIssue } from "@paygentic/sdk/funcs/entitlementsIssue.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsIssue(paygentic, {
    customerId: "cus_q3r4s5t6u7v8w9x0",
    featureId: "feat_a1b2c3d4e5f6g7h8",
    template: {
      type: "boolean",
    },
    activeFrom: new Date("2024-01-01T00:00:00Z"),
    activeTo: new Date("2025-01-01T00:00:00Z"),
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsIssue failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [models.IssueEntitlementRequest](../../models/issueentitlementrequest.md)                                                                                                      | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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
| errors.ErrorT                | 403, 404, 409                | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## get

Retrieve a specific entitlement by ID. For metered entitlements, the response includes live balance, usage, and access status for the current billing period.

### Example Usage: booleanEntitlement

<!-- UsageSnippet language="typescript" operationID="getEntitlement" method="get" path="/v1/entitlements/{entitlementId}" example="booleanEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.get({
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
import { entitlementsGet } from "@paygentic/sdk/funcs/entitlementsGet.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGet(paygentic, {
    entitlementId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGet failed:", res.error);
  }
}

run();
```
### Example Usage: meteredEntitlement

<!-- UsageSnippet language="typescript" operationID="getEntitlement" method="get" path="/v1/entitlements/{entitlementId}" example="meteredEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.get({
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
import { entitlementsGet } from "@paygentic/sdk/funcs/entitlementsGet.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGet(paygentic, {
    entitlementId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGet failed:", res.error);
  }
}

run();
```
### Example Usage: staticEntitlement

<!-- UsageSnippet language="typescript" operationID="getEntitlement" method="get" path="/v1/entitlements/{entitlementId}" example="staticEntitlement" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.entitlements.get({
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
import { entitlementsGet } from "@paygentic/sdk/funcs/entitlementsGet.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await entitlementsGet(paygentic, {
    entitlementId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("entitlementsGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetEntitlementRequest](../../models/operations/getentitlementrequest.md)                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.EntitlementDetail](../../models/entitlementdetail.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 403, 404                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |