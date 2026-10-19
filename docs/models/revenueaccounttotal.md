# RevenueAccountTotal

## Example Usage

```typescript
import { RevenueAccountTotal } from "@paygentic/sdk/models";

let value: RevenueAccountTotal = {
  currency: "Som",
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

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `currency`                                                                                                          | *string*                                                                                                            | :heavy_check_mark:                                                                                                  | ISO 4217 currency code of every amount in this entry                                                                |
| `outstanding`                                                                                                       | [models.OutstandingBlock](../models/outstandingblock.md)                                                            | :heavy_check_mark:                                                                                                  | What is owed, gross of tax, from any date. `awaitingPayment` and `paymentFailed` add up to it, in count and amount. |