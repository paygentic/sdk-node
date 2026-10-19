# Revenue

## Overview

Revenue data from invoices and payments

### Available Operations

* [get](#get) - Get revenue summary
* [getRevenueAccounts](#getrevenueaccounts) - List customer accounts

## get

Returns revenue summary with invoice and payment breakdowns (outstanding/paid/writtenOff), plus a time-series trend. Revenue is what was billed in the period (by default, invoices issued in it; see periodBasis), whatever their status since, less refunds, both excluding tax; completed payments are reported under payments, never in revenue.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getRevenue" method="get" path="/v0/revenue" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.revenue.get({
    startTime: new Date("2024-07-23T16:05:39.311Z"),
    endTime: new Date("2026-04-29T18:43:05.586Z"),
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { revenueGet } from "@paygentic/sdk/funcs/revenueGet.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await revenueGet(paygentic, {
    startTime: new Date("2024-07-23T16:05:39.311Z"),
    endTime: new Date("2026-04-29T18:43:05.586Z"),
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("revenueGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetRevenueRequest](../../models/operations/getrevenuerequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.RevenueSummaryResponse](../../models/revenuesummaryresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |

## getRevenueAccounts

Returns each customer's account as at today, one row per customer and currency, with a total per currency. Every figure covers all dates: there is no date window.

`outstanding` is what customers owe: every invoice with status `ISSUED` or `PAYMENT_FAILED`, at the amount due printed on the invoice (subtotal and tax, each rounded to the currency's minor unit), so it is gross of tax. Revenue (`GET /v0/revenue`) is net of tax. `outstanding` splits into `awaitingPayment` (status `ISSUED`) and `paymentFailed` (status `PAYMENT_FAILED`, collection has ended); the two always add up to it, in count and amount. A credit invoice (a negative amount due) nets against what is owed and is counted in no `count`; nor is an invoice whose amount due rounds to zero. A customer with nothing counted and nothing owed has no row.

Amounts are grouped by currency and never combined or converted. `totals` covers every row in the filter, not only the returned page, so the rows on one page add up to `totals` only when the page holds every row. Pages fetched in separate requests are separate reads.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getRevenueAccounts" method="get" path="/v0/revenue/accounts" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.revenue.getRevenueAccounts({
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
import { revenueGetRevenueAccounts } from "@paygentic/sdk/funcs/revenueGetRevenueAccounts.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await revenueGetRevenueAccounts(paygentic, {
    merchantId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("revenueGetRevenueAccounts failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetRevenueAccountsRequest](../../models/operations/getrevenueaccountsrequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.RevenueAccountsResponse](../../models/revenueaccountsresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403, 404                | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |