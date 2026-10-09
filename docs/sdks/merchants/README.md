# Merchants

## Overview

### Available Operations

* [reset](#reset) - Reset a merchant's data

## reset

With `scope: merchant`, deletes the merchant's customers and everything attached to them: subscriptions, invoices, line items, payments, entitlements, grants, orders, test clocks, usage events, invoice documents and, when tax is enabled, the documents in the merchant's Quaderno sandbox account. `keepCatalog: true` keeps the catalog (products, plans, prices, fees, features, billable metrics), and `keepCatalog: false` deletes it too; the merchant's configuration is always kept. With `scope: customer`, deletes one customer and what is attached to it; test clocks and the Quaderno account's documents are kept, since they belong to no single customer.

A `204` means every delete is done or scheduled: usage events and Quaderno documents finish in the background, and usage events still being ingested while it runs can survive it. A `502` means a store outside Postgres failed; the customers are already out of the API, and calling again with the same body finishes the reset. Calling again is always safe. While a customer waits for that, its external id is free for a new customer to take; a retry then deletes usage events by customer id only.

Not available in production.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="resetMerchant" method="post" path="/v0/merchants/{merchantId}/reset" -->
```typescript
import { Paygentic } from "@paygentic/sdk";

const paygentic = new Paygentic({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  await paygentic.merchants.reset({
    merchantId: "<id>",
    merchantReset: {
      scope: "merchant",
      keepCatalog: false,
    },
  });


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { PaygenticCore } from "@paygentic/sdk/core.js";
import { merchantsReset } from "@paygentic/sdk/funcs/merchantsReset.js";

// Use `PaygenticCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const paygentic = new PaygenticCore({
  bearerAuth: process.env["PAYGENTIC_BEARER_AUTH"] ?? "",
});

async function run() {
  const res = await merchantsReset(paygentic, {
    merchantId: "<id>",
    merchantReset: {
      scope: "merchant",
      keepCatalog: false,
    },
  });
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("merchantsReset failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.ResetMerchantRequest](../../models/operations/resetmerchantrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                   | Status Code                  | Content Type                 |
| ---------------------------- | ---------------------------- | ---------------------------- |
| errors.ErrorT                | 400                          | application/json             |
| errors.ValidationError       | 400                          | application/json             |
| errors.ErrorT                | 401, 403                     | application/json             |
| errors.ErrorT                | 500, 502                     | application/json             |
| errors.PaygenticDefaultError | 4XX, 5XX                     | \*/\*                        |