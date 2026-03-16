# PaymentPaid

Zero-amount Invoice 0 that completed synchronously to PAID

## Example Usage

```typescript
import { PaymentPaid } from "@paygentic/sdk/models";

let value: PaymentPaid = {
  invoiceId: "<id>",
  amount: "726.92",
  status: "paid",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `invoiceId`                                        | *string*                                           | :heavy_check_mark:                                 | The Invoice 0 id                                   |
| `amount`                                           | *string*                                           | :heavy_check_mark:                                 | Payment amount ('0' for zero-amount subscriptions) |
| `status`                                           | *"paid"*                                           | :heavy_check_mark:                                 | Payment status                                     |