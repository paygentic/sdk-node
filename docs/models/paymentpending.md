# PaymentPending

## Example Usage

```typescript
import { PaymentPending } from "@paygentic/sdk/models";

let value: PaymentPending = {
  amount: "418.24",
  breakdown: {
    upfrontCharges: "<value>",
    walletCharge: "<value>",
  },
  checkoutUrl: "https://juvenile-napkin.biz",
  paymentSessionId: "<id>",
  status: "pending",
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `amount`                                                                                                     | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Total payment amount in decimal dollar format. Sample values: '250.00' equals $250.00, '99.99' equals $99.99 |
| `breakdown`                                                                                                  | [models.Breakdown](../models/breakdown.md)                                                                   | :heavy_check_mark:                                                                                           | Breakdown of payment amount                                                                                  |
| `checkoutUrl`                                                                                                | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Checkout page URL for customer payment completion.                                                           |
| `invoiceId`                                                                                                  | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | ID of the invoice linked to this payment.                                                                    |
| `paymentSessionId`                                                                                           | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Payment session identifier for upfront payment processing.                                                   |
| `status`                                                                                                     | *"pending"*                                                                                                  | :heavy_check_mark:                                                                                           | Payment status                                                                                               |