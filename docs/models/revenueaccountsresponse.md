# RevenueAccountsResponse

## Example Usage

```typescript
import { RevenueAccountsResponse } from "@paygentic/sdk/models";

let value: RevenueAccountsResponse = {
  object: "list",
  totals: [
    {
      currency: "Bahamian Dollar",
      outstanding: {
        count: 88617,
        amount: "182.98",
        awaitingPayment: {
          count: 336537,
          amount: "852.12",
        },
        paymentFailed: {
          count: 402102,
          amount: "380.99",
        },
        overdue: {
          count: 773117,
          amount: "347.70",
        },
      },
    },
  ],
  data: [
    {
      customerId: "<id>",
      customerName: "<value>",
      currency: "Somoni",
      outstanding: {
        count: 88617,
        amount: "182.98",
        awaitingPayment: {
          count: 336537,
          amount: "852.12",
        },
        paymentFailed: {
          count: 402102,
          amount: "380.99",
        },
        overdue: {
          count: 773117,
          amount: "347.70",
        },
      },
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                                                                                                                                                                   | Type                                                                                                                                                                                                                    | Required                                                                                                                                                                                                                | Description                                                                                                                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                                                                                                                                | [models.RevenueAccountsResponseObject](../models/revenueaccountsresponseobject.md)                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                                                      | Object type identifier                                                                                                                                                                                                  |
| `totals`                                                                                                                                                                                                                | [models.RevenueAccountTotal](../models/revenueaccounttotal.md)[]                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                                                                      | One entry per currency with at least one row in the filter, over every row and not only this page. The merchant's primary currency comes first, then the rest in alphabetical order. Empty when there are no rows.      |
| `data`                                                                                                                                                                                                                  | [models.RevenueAccountRow](../models/revenueaccountrow.md)[]                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                                                                      | One row per customer and currency with at least one unpaid invoice, in the currency order of `totals`, then by `outstanding.amount` descending, then by `customerId`. A customer billed in two currencies has two rows. |
| `pagination`                                                                                                                                                                                                            | [models.OffsetPagination](../models/offsetpagination.md)                                                                                                                                                                | :heavy_check_mark:                                                                                                                                                                                                      | Offset-based pagination response.                                                                                                                                                                                       |