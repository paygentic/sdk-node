# paygentic

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *paygentic* API.

<div align="left">
    <a href="https://www.speakeasy.com/?utm_source=paygentic&utm_campaign=typescript"><img src="https://www.speakeasy.com/assets/badges/built-by-speakeasy.svg" /></a>
    <a href="https://opensource.org/licenses/MIT">
        <img src="https://img.shields.io/badge/License-MIT-blue.svg" style="width: 100px; height: 28px;" />
    </a>
</div>


<br /><br />
<!-- Start Summary [summary] -->
## Summary

Paygentic API: The Paygentic API provides a comprehensive platform for building and scaling monetization infrastructure.

## Authentication
All API requests require authentication using an API key passed in the `Authorization` header:
```
Authorization: Bearer YOUR_API_KEY
```

## Base URL
All API requests should be made to:
```
https://api.paygentic.io/v0
```
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [paygentic](#paygentic)
  * [Authentication](#authentication)
  * [Base URL](#base-url)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication-1)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add @paygentic/sdk
```

### PNPM

```bash
pnpm add @paygentic/sdk
```

### Bun

```bash
bun add @paygentic/sdk
```

### Yarn

```bash
yarn add @paygentic/sdk
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.create({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  });

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type | Scheme      | Environment Variable    |
| ------------ | ---- | ----------- | ----------------------- |
| `bearerAuth` | http | HTTP Bearer | `PAYGENTIC_BEARER_AUTH` |

To authenticate with the API the `bearerAuth` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.create({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  });

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [BillableMetrics](docs/sdks/billablemetrics/README.md)

* [create](docs/sdks/billablemetrics/README.md#create) - Create
* [list](docs/sdks/billablemetrics/README.md#list) - List
* [get](docs/sdks/billablemetrics/README.md#get) - Get
* [update](docs/sdks/billablemetrics/README.md#update) - Update

### [Customers](docs/sdks/customers/README.md)

* [list](docs/sdks/customers/README.md#list) - List by Merchant
* [create](docs/sdks/customers/README.md#create) - Create
* [get](docs/sdks/customers/README.md#get) - Get
* [update](docs/sdks/customers/README.md#update) - Update

### [Disputes](docs/sdks/disputes/README.md)

* [create](docs/sdks/disputes/README.md#create) - Create
* [list](docs/sdks/disputes/README.md#list) - List

### [Entitlements](docs/sdks/entitlements/README.md)

* [listActive](docs/sdks/entitlements/README.md#listactive) - List by Customer
* [create](docs/sdks/entitlements/README.md#create) - Create
* [list](docs/sdks/entitlements/README.md#list) - List Entitlements

### [Features](docs/sdks/features/README.md)

* [list](docs/sdks/features/README.md#list) - List
* [create](docs/sdks/features/README.md#create) - Create
* [get](docs/sdks/features/README.md#get) - Get
* [update](docs/sdks/features/README.md#update) - Update
* [delete](docs/sdks/features/README.md#delete) - Delete

### [Fees](docs/sdks/fees/README.md)

* [create](docs/sdks/fees/README.md#create) - Create
* [list](docs/sdks/fees/README.md#list) - List
* [get](docs/sdks/fees/README.md#get) - Get
* [update](docs/sdks/fees/README.md#update) - Update
* [delete](docs/sdks/fees/README.md#delete) - Delete
* [getPrice](docs/sdks/fees/README.md#getprice) - Get Fee Price

### [InvoicesV2](docs/sdks/invoicesv2/README.md)

* [list](docs/sdks/invoicesv2/README.md#list) - List
* [get](docs/sdks/invoicesv2/README.md#get) - Get
* [getLineItems](docs/sdks/invoicesv2/README.md#getlineitems) - Get Line Items

### [Plans](docs/sdks/plans/README.md)

* [create](docs/sdks/plans/README.md#create) - Create
* [list](docs/sdks/plans/README.md#list) - List
* [listAvailable](docs/sdks/plans/README.md#listavailable) - List Available Plans
* [get](docs/sdks/plans/README.md#get) - Get
* [update](docs/sdks/plans/README.md#update) - Update

### [Prices](docs/sdks/prices/README.md)

* [create](docs/sdks/prices/README.md#create) - Create
* [list](docs/sdks/prices/README.md#list) - List
* [get](docs/sdks/prices/README.md#get) - Get
* [update](docs/sdks/prices/README.md#update) - Update
* [delete](docs/sdks/prices/README.md#delete) - Delete

### [Products](docs/sdks/products/README.md)

* [create](docs/sdks/products/README.md#create) - Create
* [list](docs/sdks/products/README.md#list) - List
* [get](docs/sdks/products/README.md#get) - Get
* [update](docs/sdks/products/README.md#update) - Update

### [Revenue](docs/sdks/revenue/README.md)

* [get](docs/sdks/revenue/README.md#get) - Get revenue time series

### [Sources](docs/sdks/sources/README.md)

* [create](docs/sdks/sources/README.md#create) - Create
* [list](docs/sdks/sources/README.md#list) - List
* [get](docs/sdks/sources/README.md#get) - Get
* [update](docs/sdks/sources/README.md#update) - Update

### [Sources.Events](docs/sdks/events/README.md)

* [list](docs/sdks/events/README.md#list) - List Events
* [approve](docs/sdks/events/README.md#approve) - Approve
* [reject](docs/sdks/events/README.md#reject) - Reject
* [bulkApprove](docs/sdks/events/README.md#bulkapprove) - Bulk Approve
* [bulkReject](docs/sdks/events/README.md#bulkreject) - Bulk Reject

### [Sources.Rules](docs/sdks/rules/README.md)

* [list](docs/sdks/rules/README.md#list) - List Rules
* [create](docs/sdks/rules/README.md#create) - Create Rule
* [get](docs/sdks/rules/README.md#get) - Get Rule
* [update](docs/sdks/rules/README.md#update) - Update Rule
* [delete](docs/sdks/rules/README.md#delete) - Delete Rule

### [Subscriptions](docs/sdks/subscriptions/README.md)

* [list](docs/sdks/subscriptions/README.md#list) - List
* [create](docs/sdks/subscriptions/README.md#create) - Create
* [get](docs/sdks/subscriptions/README.md#get) - Get
* [generatePortalLink](docs/sdks/subscriptions/README.md#generateportallink) - Generate Portal Link
* [terminate](docs/sdks/subscriptions/README.md#terminate) - Terminate

### [TestClocks](docs/sdks/testclocks/README.md)

* [list](docs/sdks/testclocks/README.md#list) - List
* [create](docs/sdks/testclocks/README.md#create) - Create
* [get](docs/sdks/testclocks/README.md#get) - Get
* [advance](docs/sdks/testclocks/README.md#advance) - Advance
* [delete](docs/sdks/testclocks/README.md#delete) - Delete

### [UsageEvents](docs/sdks/usageevents/README.md)

* [create](docs/sdks/usageevents/README.md#create) - Create
* [list](docs/sdks/usageevents/README.md#list) - List
* [get](docs/sdks/usageevents/README.md#get) - Get
* [refund](docs/sdks/usageevents/README.md#refund) - Refund
* [batchCreate](docs/sdks/usageevents/README.md#batchcreate) - Batch Create

### [Users](docs/sdks/users/README.md)

* [get](docs/sdks/users/README.md#get) - Get
* [update](docs/sdks/users/README.md#update) - Update

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`billableMetricsCreate`](docs/sdks/billablemetrics/README.md#create) - Create
- [`billableMetricsGet`](docs/sdks/billablemetrics/README.md#get) - Get
- [`billableMetricsList`](docs/sdks/billablemetrics/README.md#list) - List
- [`billableMetricsUpdate`](docs/sdks/billablemetrics/README.md#update) - Update
- [`customersCreate`](docs/sdks/customers/README.md#create) - Create
- [`customersGet`](docs/sdks/customers/README.md#get) - Get
- [`customersList`](docs/sdks/customers/README.md#list) - List by Merchant
- [`customersUpdate`](docs/sdks/customers/README.md#update) - Update
- [`disputesCreate`](docs/sdks/disputes/README.md#create) - Create
- [`disputesList`](docs/sdks/disputes/README.md#list) - List
- [`entitlementsCreate`](docs/sdks/entitlements/README.md#create) - Create
- [`entitlementsList`](docs/sdks/entitlements/README.md#list) - List Entitlements
- [`entitlementsListActive`](docs/sdks/entitlements/README.md#listactive) - List by Customer
- [`featuresCreate`](docs/sdks/features/README.md#create) - Create
- [`featuresDelete`](docs/sdks/features/README.md#delete) - Delete
- [`featuresGet`](docs/sdks/features/README.md#get) - Get
- [`featuresList`](docs/sdks/features/README.md#list) - List
- [`featuresUpdate`](docs/sdks/features/README.md#update) - Update
- [`feesCreate`](docs/sdks/fees/README.md#create) - Create
- [`feesDelete`](docs/sdks/fees/README.md#delete) - Delete
- [`feesGet`](docs/sdks/fees/README.md#get) - Get
- [`feesGetPrice`](docs/sdks/fees/README.md#getprice) - Get Fee Price
- [`feesList`](docs/sdks/fees/README.md#list) - List
- [`feesUpdate`](docs/sdks/fees/README.md#update) - Update
- [`invoicesV2Get`](docs/sdks/invoicesv2/README.md#get) - Get
- [`invoicesV2GetLineItems`](docs/sdks/invoicesv2/README.md#getlineitems) - Get Line Items
- [`invoicesV2List`](docs/sdks/invoicesv2/README.md#list) - List
- [`plansCreate`](docs/sdks/plans/README.md#create) - Create
- [`plansGet`](docs/sdks/plans/README.md#get) - Get
- [`plansList`](docs/sdks/plans/README.md#list) - List
- [`plansListAvailable`](docs/sdks/plans/README.md#listavailable) - List Available Plans
- [`plansUpdate`](docs/sdks/plans/README.md#update) - Update
- [`pricesCreate`](docs/sdks/prices/README.md#create) - Create
- [`pricesDelete`](docs/sdks/prices/README.md#delete) - Delete
- [`pricesGet`](docs/sdks/prices/README.md#get) - Get
- [`pricesList`](docs/sdks/prices/README.md#list) - List
- [`pricesUpdate`](docs/sdks/prices/README.md#update) - Update
- [`productsCreate`](docs/sdks/products/README.md#create) - Create
- [`productsGet`](docs/sdks/products/README.md#get) - Get
- [`productsList`](docs/sdks/products/README.md#list) - List
- [`productsUpdate`](docs/sdks/products/README.md#update) - Update
- [`revenueGet`](docs/sdks/revenue/README.md#get) - Get revenue time series
- [`sourcesCreate`](docs/sdks/sources/README.md#create) - Create
- [`sourcesEventsApprove`](docs/sdks/events/README.md#approve) - Approve
- [`sourcesEventsBulkApprove`](docs/sdks/events/README.md#bulkapprove) - Bulk Approve
- [`sourcesEventsBulkReject`](docs/sdks/events/README.md#bulkreject) - Bulk Reject
- [`sourcesEventsList`](docs/sdks/events/README.md#list) - List Events
- [`sourcesEventsReject`](docs/sdks/events/README.md#reject) - Reject
- [`sourcesGet`](docs/sdks/sources/README.md#get) - Get
- [`sourcesList`](docs/sdks/sources/README.md#list) - List
- [`sourcesRulesCreate`](docs/sdks/rules/README.md#create) - Create Rule
- [`sourcesRulesDelete`](docs/sdks/rules/README.md#delete) - Delete Rule
- [`sourcesRulesGet`](docs/sdks/rules/README.md#get) - Get Rule
- [`sourcesRulesList`](docs/sdks/rules/README.md#list) - List Rules
- [`sourcesRulesUpdate`](docs/sdks/rules/README.md#update) - Update Rule
- [`sourcesUpdate`](docs/sdks/sources/README.md#update) - Update
- [`subscriptionsCreate`](docs/sdks/subscriptions/README.md#create) - Create
- [`subscriptionsGeneratePortalLink`](docs/sdks/subscriptions/README.md#generateportallink) - Generate Portal Link
- [`subscriptionsGet`](docs/sdks/subscriptions/README.md#get) - Get
- [`subscriptionsList`](docs/sdks/subscriptions/README.md#list) - List
- [`subscriptionsTerminate`](docs/sdks/subscriptions/README.md#terminate) - Terminate
- [`testClocksAdvance`](docs/sdks/testclocks/README.md#advance) - Advance
- [`testClocksCreate`](docs/sdks/testclocks/README.md#create) - Create
- [`testClocksDelete`](docs/sdks/testclocks/README.md#delete) - Delete
- [`testClocksGet`](docs/sdks/testclocks/README.md#get) - Get
- [`testClocksList`](docs/sdks/testclocks/README.md#list) - List
- [`usageEventsBatchCreate`](docs/sdks/usageevents/README.md#batchcreate) - Batch Create
- [`usageEventsCreate`](docs/sdks/usageevents/README.md#create) - Create
- [`usageEventsGet`](docs/sdks/usageevents/README.md#get) - Get
- [`usageEventsList`](docs/sdks/usageevents/README.md#list) - List
- [`usageEventsRefund`](docs/sdks/usageevents/README.md#refund) - Refund
- [`usersGet`](docs/sdks/users/README.md#get) - Get
- [`usersUpdate`](docs/sdks/users/README.md#update) - Update

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.create({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  }, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.create({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  });

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`PaygenticError`](./src/models/errors/paygenticerror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { Paygentic } from "@paygentic/sdk";
import * as errors from "@paygentic/sdk/models/errors";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  try {
    const result = await paygentic.billableMetrics.create({
      aggregation: "SUM",
      description: "other gracefully hold",
      merchantId: "<id>",
      name: "<value>",
      productId: "<id>",
      unit: "becquerel",
    });

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.PaygenticError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.ErrorT) {
        console.log(error.data$.error); // string
        console.log(error.data$.message); // string
        console.log(error.data$.details); // { [k: string]: any }
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`PaygenticError`](./src/models/errors/paygenticerror.ts): The base class for HTTP error responses.
  * [`ErrorT`](./src/models/errors/errort.ts): Generic error.

<details><summary>Less common errors (8)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`PaygenticError`](./src/models/errors/paygenticerror.ts)**:
* [`ValidationError`](./src/models/errors/validationerror.ts): Bad Request - The request could not be understood or was missing required parameters. Status code `400`. Applicable to 43 of 73 methods.*
* [`ConflictError`](./src/models/errors/conflicterror.ts): Fee cannot be deleted because it has associated prices. Status code `409`. Applicable to 1 of 73 methods.*
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>

\* Check [the method documentation](#available-resources-and-operations) to see if the error is applicable.
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  serverURL: "https://api.paygentic.io",
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.billableMetrics.create({
    aggregation: "SUM",
    description: "other gracefully hold",
    merchantId: "<id>",
    name: "<value>",
    productId: "<id>",
    unit: "becquerel",
  });

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to:
- route requests through a proxy server using [undici](https://www.npmjs.com/package/undici)'s ProxyAgent
- use the `"beforeRequest"` hook to add a custom header and a timeout to requests
- use the `"requestError"` hook to log errors

```typescript
import { Paygentic } from "@paygentic/sdk";
import { ProxyAgent } from "undici";
import { HTTPClient } from "@paygentic/sdk/lib/http";

const dispatcher = new ProxyAgent("http://proxy.example.com:8080");

const httpClient = new HTTPClient({
  // 'fetcher' takes a function that has the same signature as native 'fetch'.
  fetcher: (input, init) =>
    // 'dispatcher' is specific to undici and not part of the standard Fetch API.
    fetch(input, { ...init, dispatcher } as RequestInit),
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new Paygentic({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { Paygentic } from "@paygentic/sdk";

const sdk = new Paygentic({ debugLogger: console });
```

You can also enable a default debug logger by setting an environment variable `PAYGENTIC_DEBUG` to true.
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 

### SDK Created by [Speakeasy](https://www.speakeasy.com/?utm_source=paygentic&utm_campaign=typescript)
