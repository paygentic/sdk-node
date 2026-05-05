# Profitability

## Overview

Per-customer profitability summaries

### Available Operations

* [getProfitability](#getprofitability) - Get profitability summary

## getProfitability

Returns a per-customer profitability summary for a merchant over a date range. Each row aggregates revenue (from issued + paid invoices), cost (from metered cost discovery), profit, and margin. Customers are ranked by profit descending and capped at topN; the remainder is rolled into a single self-consistent 'Other' row whose revenue, cost, and profit reflect the same set of customers. Rows are inner-joined against the merchant's customer list, so orphaned meter subjects from deleted or unknown customers are dropped.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="getProfitability" method="get" path="/v0/profitability" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const result = await paygentic.profitability.getProfitability({
    merchantId: "<id>",
    from: new Date("2026-09-10T15:32:06.535Z"),
    to: new Date("2026-10-20T08:45:45.521Z"),
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { profitabilityGetProfitability } from "@paygentic/sdk/funcs/profitabilityGetProfitability.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await profitabilityGetProfitability(paygentic, {
    merchantId: "<id>",
    from: new Date("2026-09-10T15:32:06.535Z"),
    to: new Date("2026-10-20T08:45:45.521Z"),
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("profitabilityGetProfitability failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetProfitabilityRequest](../../models/operations/getprofitabilityrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[models.ProfitabilitySummaryResponse](../../models/profitabilitysummaryresponse.md)\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403                     | application/json             |
| errors.ErrorT                | 500                          | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |