# PoolGrantPurchaseResponsePaymentSession

## Example Usage

```typescript
import { PoolGrantPurchaseResponsePaymentSession } from "@paygentic/sdk/models";

let value: PoolGrantPurchaseResponsePaymentSession = {
  url: "https://rusty-window.com/",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | The Stripe checkout URL for the customer to complete payment.                                 |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the payment session expires.                                                             |
| `amount`                                                                                      | *number*                                                                                      | :heavy_minus_sign:                                                                            | The payment amount in the currency's minor unit (e.g., cents).                                |