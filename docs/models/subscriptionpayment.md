# SubscriptionPayment

Payment session details when upfront payment is required

## Example Usage

```typescript
import { SubscriptionPayment } from "@paygentic/sdk/models";

let value: SubscriptionPayment = {
  amount: "400.56",
  breakdown: {
    upfrontCharges: "<value>",
    walletCharge: "<value>",
  },
  checkoutUrl: "https://gripping-characterization.com",
  paymentSessionId: "<id>",
  status: "pending",
};
```

## Fields

| Field                                                                                                                                                           | Type                                                                                                                                                            | Required                                                                                                                                                        | Description                                                                                                                                                     |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                                                                        | *string*                                                                                                                                                        | :heavy_check_mark:                                                                                                                                              | Total payment amount in decimal dollar format. Sample values: '250.00' equals $250.00, '99.99' equals $99.99                                                    |
| `breakdown`                                                                                                                                                     | [models.Breakdown](../models/breakdown.md)                                                                                                                      | :heavy_check_mark:                                                                                                                                              | Breakdown of payment amount                                                                                                                                     |
| `checkoutUrl`                                                                                                                                                   | *string*                                                                                                                                                        | :heavy_check_mark:                                                                                                                                              | Checkout page URL for customer payment completion. Sample values: 'https://checkout.paygentic.com/session/ps_abc123', 'https://pay.example.com/checkout/xyz789' |
| `invoiceId`                                                                                                                                                     | *string*                                                                                                                                                        | :heavy_minus_sign:                                                                                                                                              | ID of the invoice linked to this payment.                                                                                                                       |
| `paymentSessionId`                                                                                                                                              | *string*                                                                                                                                                        | :heavy_check_mark:                                                                                                                                              | Payment session identifier for upfront payment processing. Sample values: 'ps_abc123xyz', 'ps_789def456'                                                        |
| `status`                                                                                                                                                        | [models.StatusPending](../models/statuspending.md)                                                                                                              | :heavy_check_mark:                                                                                                                                              | Payment status                                                                                                                                                  |