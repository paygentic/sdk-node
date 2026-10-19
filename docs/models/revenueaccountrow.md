# RevenueAccountRow

## Example Usage

```typescript
import { RevenueAccountRow } from "@paygentic/sdk/models";

let value: RevenueAccountRow = {
  customerId: "<id>",
  customerName: "<value>",
  currency: "Malagasy Ariary",
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
  },
};
```

## Fields

| Field                                                                                                                      | Type                                                                                                                       | Required                                                                                                                   | Description                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `customerId`                                                                                                               | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | Customer ID                                                                                                                |
| `customerName`                                                                                                             | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | Customer display name, or the customer ID when no name is recorded. A deleted customer who still owes money keeps its row. |
| `currency`                                                                                                                 | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | ISO 4217 currency code of every amount in this row                                                                         |
| `outstanding`                                                                                                              | [models.OutstandingBlock](../models/outstandingblock.md)                                                                   | :heavy_check_mark:                                                                                                         | What is owed, gross of tax, from any date. `awaitingPayment` and `paymentFailed` add up to it, in count and amount.        |