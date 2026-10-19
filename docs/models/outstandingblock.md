# OutstandingBlock

What is owed, gross of tax, from any date. `awaitingPayment` and `paymentFailed` add up to it, in count and amount.

## Example Usage

```typescript
import { OutstandingBlock } from "@paygentic/sdk/models";

let value: OutstandingBlock = {
  count: 312281,
  amount: "831.31",
  awaitingPayment: {
    count: 336537,
    amount: "852.12",
  },
  paymentFailed: {
    count: 402102,
    amount: "380.99",
  },
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `count`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Number of unpaid invoices with an amount due above zero. A credit invoice, or one whose amount due rounds to zero, is not counted.        |
| `amount`                                                                                                                                  | *string*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total amount due in major units of the currency, in its decimal places (for example "123.00"). Negative when credits exceed what is owed. |
| `awaitingPayment`                                                                                                                         | [models.AccountFigure](../models/accountfigure.md)                                                                                        | :heavy_check_mark:                                                                                                                        | The part with status `ISSUED`, including any credit invoice                                                                               |
| `paymentFailed`                                                                                                                           | [models.AccountFigure](../models/accountfigure.md)                                                                                        | :heavy_check_mark:                                                                                                                        | The part with status `PAYMENT_FAILED`: collection has ended                                                                               |