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
  const result = await paygentic.billableMetrics.createBillableMetric({
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
  const result = await paygentic.billableMetrics.createBillableMetric({
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

* [createBillableMetric](docs/sdks/billablemetrics/README.md#createbillablemetric) - Create
* [listBillableMetrics](docs/sdks/billablemetrics/README.md#listbillablemetrics) - List
* [getBillableMetric](docs/sdks/billablemetrics/README.md#getbillablemetric) - Get
* [updateBillableMetric](docs/sdks/billablemetrics/README.md#updatebillablemetric) - Update

### [Customers](docs/sdks/customers/README.md)

* [listCustomers](docs/sdks/customers/README.md#listcustomers) - List by Merchant
* [createCustomer](docs/sdks/customers/README.md#createcustomer) - Create
* [getCustomer](docs/sdks/customers/README.md#getcustomer) - Get
* [updateCustomer](docs/sdks/customers/README.md#updatecustomer) - Update

### [Disputes](docs/sdks/disputes/README.md)

* [createDispute](docs/sdks/disputes/README.md#createdispute) - Create
* [listDisputes](docs/sdks/disputes/README.md#listdisputes) - List

### [Entitlements](docs/sdks/entitlements/README.md)

* [getActiveEntitlements](docs/sdks/entitlements/README.md#getactiveentitlements) - List by Customer
* [createEntitlement](docs/sdks/entitlements/README.md#createentitlement) - Create
* [listEntitlements](docs/sdks/entitlements/README.md#listentitlements) - List Entitlements

### [Features](docs/sdks/features/README.md)

* [listFeatures](docs/sdks/features/README.md#listfeatures) - List
* [createFeature](docs/sdks/features/README.md#createfeature) - Create
* [getFeature](docs/sdks/features/README.md#getfeature) - Get
* [updateFeature](docs/sdks/features/README.md#updatefeature) - Update
* [deleteFeature](docs/sdks/features/README.md#deletefeature) - Delete

### [Fees](docs/sdks/fees/README.md)

* [createFee](docs/sdks/fees/README.md#createfee) - Create
* [listFees](docs/sdks/fees/README.md#listfees) - List
* [getFee](docs/sdks/fees/README.md#getfee) - Get
* [updateFee](docs/sdks/fees/README.md#updatefee) - Update
* [deleteFee](docs/sdks/fees/README.md#deletefee) - Delete
* [getFeePrice](docs/sdks/fees/README.md#getfeeprice) - Get Fee Price

### [InvoicesV2](docs/sdks/invoicesv2/README.md)

* [listInvoices](docs/sdks/invoicesv2/README.md#listinvoices) - List
* [getInvoice](docs/sdks/invoicesv2/README.md#getinvoice) - Get
* [getInvoiceLineItems](docs/sdks/invoicesv2/README.md#getinvoicelineitems) - Get Line Items

### [Plans](docs/sdks/plans/README.md)

* [createPlan](docs/sdks/plans/README.md#createplan) - Create
* [listPlans](docs/sdks/plans/README.md#listplans) - List
* [listAvailablePlans](docs/sdks/plans/README.md#listavailableplans) - List Available Plans
* [getPlan](docs/sdks/plans/README.md#getplan) - Get
* [updatePlan](docs/sdks/plans/README.md#updateplan) - Update

### [Prices](docs/sdks/prices/README.md)

* [createPrice](docs/sdks/prices/README.md#createprice) - Create
* [listPrices](docs/sdks/prices/README.md#listprices) - List
* [getPrice](docs/sdks/prices/README.md#getprice) - Get
* [updatePrice](docs/sdks/prices/README.md#updateprice) - Update
* [deletePrice](docs/sdks/prices/README.md#deleteprice) - Delete

### [Products](docs/sdks/products/README.md)

* [createProduct](docs/sdks/products/README.md#createproduct) - Create
* [listProducts](docs/sdks/products/README.md#listproducts) - List
* [getProduct](docs/sdks/products/README.md#getproduct) - Get
* [updateProduct](docs/sdks/products/README.md#updateproduct) - Update

### [Revenue](docs/sdks/revenue/README.md)

* [getRevenue](docs/sdks/revenue/README.md#getrevenue) - Get revenue time series

### [Sources](docs/sdks/sources/README.md)

* [createSource](docs/sdks/sources/README.md#createsource) - Create
* [listSources](docs/sdks/sources/README.md#listsources) - List
* [getSource](docs/sdks/sources/README.md#getsource) - Get
* [updateSource](docs/sdks/sources/README.md#updatesource) - Update
* [listSourceEvents](docs/sdks/sources/README.md#listsourceevents) - List Events
* [approveSourceEvent](docs/sdks/sources/README.md#approvesourceevent) - Approve
* [rejectSourceEvent](docs/sdks/sources/README.md#rejectsourceevent) - Reject
* [bulkApproveSourceEvents](docs/sdks/sources/README.md#bulkapprovesourceevents) - Bulk Approve
* [bulkRejectSourceEvents](docs/sdks/sources/README.md#bulkrejectsourceevents) - Bulk Reject
* [listSourceRules](docs/sdks/sources/README.md#listsourcerules) - List Rules
* [createSourceRule](docs/sdks/sources/README.md#createsourcerule) - Create Rule
* [getSourceRule](docs/sdks/sources/README.md#getsourcerule) - Get Rule
* [updateSourceRule](docs/sdks/sources/README.md#updatesourcerule) - Update Rule
* [deleteSourceRule](docs/sdks/sources/README.md#deletesourcerule) - Delete Rule

### [Subscriptions](docs/sdks/subscriptions/README.md)

* [listSubscriptions](docs/sdks/subscriptions/README.md#listsubscriptions) - List
* [createSubscription](docs/sdks/subscriptions/README.md#createsubscription) - Create
* [getSubscription](docs/sdks/subscriptions/README.md#getsubscription) - Get
* [generatePortalLink](docs/sdks/subscriptions/README.md#generateportallink) - Generate Portal Link
* [terminateSubscription](docs/sdks/subscriptions/README.md#terminatesubscription) - Terminate

### [TestClocks](docs/sdks/testclocks/README.md)

* [listTestClocks](docs/sdks/testclocks/README.md#listtestclocks) - List
* [createTestClock](docs/sdks/testclocks/README.md#createtestclock) - Create
* [getTestClock](docs/sdks/testclocks/README.md#gettestclock) - Get
* [advanceTestClock](docs/sdks/testclocks/README.md#advancetestclock) - Advance
* [deleteTestClock](docs/sdks/testclocks/README.md#deletetestclock) - Delete

### [UsageEvents](docs/sdks/usageevents/README.md)

* [createUsageEvent](docs/sdks/usageevents/README.md#createusageevent) - Create
* [listUsageEvents](docs/sdks/usageevents/README.md#listusageevents) - List
* [getUsageEvent](docs/sdks/usageevents/README.md#getusageevent) - Get
* [refundUsageEvent](docs/sdks/usageevents/README.md#refundusageevent) - Refund
* [batchCreateUsageEvents](docs/sdks/usageevents/README.md#batchcreateusageevents) - Batch Create

### [Users](docs/sdks/users/README.md)

* [getUser](docs/sdks/users/README.md#getuser) - Get
* [updateUser](docs/sdks/users/README.md#updateuser) - Update

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

- [`billableMetricsCreateBillableMetric`](docs/sdks/billablemetrics/README.md#createbillablemetric) - Create
- [`billableMetricsGetBillableMetric`](docs/sdks/billablemetrics/README.md#getbillablemetric) - Get
- [`billableMetricsListBillableMetrics`](docs/sdks/billablemetrics/README.md#listbillablemetrics) - List
- [`billableMetricsUpdateBillableMetric`](docs/sdks/billablemetrics/README.md#updatebillablemetric) - Update
- [`customersCreateCustomer`](docs/sdks/customers/README.md#createcustomer) - Create
- [`customersGetCustomer`](docs/sdks/customers/README.md#getcustomer) - Get
- [`customersListCustomers`](docs/sdks/customers/README.md#listcustomers) - List by Merchant
- [`customersUpdateCustomer`](docs/sdks/customers/README.md#updatecustomer) - Update
- [`disputesCreateDispute`](docs/sdks/disputes/README.md#createdispute) - Create
- [`disputesListDisputes`](docs/sdks/disputes/README.md#listdisputes) - List
- [`entitlementsCreateEntitlement`](docs/sdks/entitlements/README.md#createentitlement) - Create
- [`entitlementsGetActiveEntitlements`](docs/sdks/entitlements/README.md#getactiveentitlements) - List by Customer
- [`entitlementsListEntitlements`](docs/sdks/entitlements/README.md#listentitlements) - List Entitlements
- [`featuresCreateFeature`](docs/sdks/features/README.md#createfeature) - Create
- [`featuresDeleteFeature`](docs/sdks/features/README.md#deletefeature) - Delete
- [`featuresGetFeature`](docs/sdks/features/README.md#getfeature) - Get
- [`featuresListFeatures`](docs/sdks/features/README.md#listfeatures) - List
- [`featuresUpdateFeature`](docs/sdks/features/README.md#updatefeature) - Update
- [`feesCreateFee`](docs/sdks/fees/README.md#createfee) - Create
- [`feesDeleteFee`](docs/sdks/fees/README.md#deletefee) - Delete
- [`feesGetFee`](docs/sdks/fees/README.md#getfee) - Get
- [`feesGetFeePrice`](docs/sdks/fees/README.md#getfeeprice) - Get Fee Price
- [`feesListFees`](docs/sdks/fees/README.md#listfees) - List
- [`feesUpdateFee`](docs/sdks/fees/README.md#updatefee) - Update
- [`invoicesV2GetInvoice`](docs/sdks/invoicesv2/README.md#getinvoice) - Get
- [`invoicesV2GetInvoiceLineItems`](docs/sdks/invoicesv2/README.md#getinvoicelineitems) - Get Line Items
- [`invoicesV2ListInvoices`](docs/sdks/invoicesv2/README.md#listinvoices) - List
- [`plansCreatePlan`](docs/sdks/plans/README.md#createplan) - Create
- [`plansGetPlan`](docs/sdks/plans/README.md#getplan) - Get
- [`plansListAvailablePlans`](docs/sdks/plans/README.md#listavailableplans) - List Available Plans
- [`plansListPlans`](docs/sdks/plans/README.md#listplans) - List
- [`plansUpdatePlan`](docs/sdks/plans/README.md#updateplan) - Update
- [`pricesCreatePrice`](docs/sdks/prices/README.md#createprice) - Create
- [`pricesDeletePrice`](docs/sdks/prices/README.md#deleteprice) - Delete
- [`pricesGetPrice`](docs/sdks/prices/README.md#getprice) - Get
- [`pricesListPrices`](docs/sdks/prices/README.md#listprices) - List
- [`pricesUpdatePrice`](docs/sdks/prices/README.md#updateprice) - Update
- [`productsCreateProduct`](docs/sdks/products/README.md#createproduct) - Create
- [`productsGetProduct`](docs/sdks/products/README.md#getproduct) - Get
- [`productsListProducts`](docs/sdks/products/README.md#listproducts) - List
- [`productsUpdateProduct`](docs/sdks/products/README.md#updateproduct) - Update
- [`revenueGetRevenue`](docs/sdks/revenue/README.md#getrevenue) - Get revenue time series
- [`sourcesApproveSourceEvent`](docs/sdks/sources/README.md#approvesourceevent) - Approve
- [`sourcesBulkApproveSourceEvents`](docs/sdks/sources/README.md#bulkapprovesourceevents) - Bulk Approve
- [`sourcesBulkRejectSourceEvents`](docs/sdks/sources/README.md#bulkrejectsourceevents) - Bulk Reject
- [`sourcesCreateSource`](docs/sdks/sources/README.md#createsource) - Create
- [`sourcesCreateSourceRule`](docs/sdks/sources/README.md#createsourcerule) - Create Rule
- [`sourcesDeleteSourceRule`](docs/sdks/sources/README.md#deletesourcerule) - Delete Rule
- [`sourcesGetSource`](docs/sdks/sources/README.md#getsource) - Get
- [`sourcesGetSourceRule`](docs/sdks/sources/README.md#getsourcerule) - Get Rule
- [`sourcesListSourceEvents`](docs/sdks/sources/README.md#listsourceevents) - List Events
- [`sourcesListSourceRules`](docs/sdks/sources/README.md#listsourcerules) - List Rules
- [`sourcesListSources`](docs/sdks/sources/README.md#listsources) - List
- [`sourcesRejectSourceEvent`](docs/sdks/sources/README.md#rejectsourceevent) - Reject
- [`sourcesUpdateSource`](docs/sdks/sources/README.md#updatesource) - Update
- [`sourcesUpdateSourceRule`](docs/sdks/sources/README.md#updatesourcerule) - Update Rule
- [`subscriptionsCreateSubscription`](docs/sdks/subscriptions/README.md#createsubscription) - Create
- [`subscriptionsGeneratePortalLink`](docs/sdks/subscriptions/README.md#generateportallink) - Generate Portal Link
- [`subscriptionsGetSubscription`](docs/sdks/subscriptions/README.md#getsubscription) - Get
- [`subscriptionsListSubscriptions`](docs/sdks/subscriptions/README.md#listsubscriptions) - List
- [`subscriptionsTerminateSubscription`](docs/sdks/subscriptions/README.md#terminatesubscription) - Terminate
- [`testClocksAdvanceTestClock`](docs/sdks/testclocks/README.md#advancetestclock) - Advance
- [`testClocksCreateTestClock`](docs/sdks/testclocks/README.md#createtestclock) - Create
- [`testClocksDeleteTestClock`](docs/sdks/testclocks/README.md#deletetestclock) - Delete
- [`testClocksGetTestClock`](docs/sdks/testclocks/README.md#gettestclock) - Get
- [`testClocksListTestClocks`](docs/sdks/testclocks/README.md#listtestclocks) - List
- [`usageEventsBatchCreateUsageEvents`](docs/sdks/usageevents/README.md#batchcreateusageevents) - Batch Create
- [`usageEventsCreateUsageEvent`](docs/sdks/usageevents/README.md#createusageevent) - Create
- [`usageEventsGetUsageEvent`](docs/sdks/usageevents/README.md#getusageevent) - Get
- [`usageEventsListUsageEvents`](docs/sdks/usageevents/README.md#listusageevents) - List
- [`usageEventsRefundUsageEvent`](docs/sdks/usageevents/README.md#refundusageevent) - Refund
- [`usersGetUser`](docs/sdks/users/README.md#getuser) - Get
- [`usersUpdateUser`](docs/sdks/users/README.md#updateuser) - Update

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
  const result = await paygentic.billableMetrics.createBillableMetric({
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
  const result = await paygentic.billableMetrics.createBillableMetric({
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
    const result = await paygentic.billableMetrics.createBillableMetric({
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
  const result = await paygentic.billableMetrics.createBillableMetric({
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
