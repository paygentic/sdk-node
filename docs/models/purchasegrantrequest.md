# PurchaseGrantRequest

## Example Usage

```typescript
import { PurchaseGrantRequest } from "@paygentic/sdk/models";

let value: PurchaseGrantRequest = {
  amount: 957.01,
  price: "97.99",
  idempotencyKey: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | The number of credits to grant upon payment completion.                                       |
| `price`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | The price in decimal format (e.g., '5.00' for $5.00 USD). Must be at least $0.50.             |
| `idempotencyKey`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Caller-provided deduplication key. Retrying with the same key returns the existing invoice.   |
| `effectiveAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the grant becomes effective. Defaults to now.                                            |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the grant expires. If omitted, the grant does not expire.                                |
| `successUrl`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | URL to redirect the customer to after successful payment.                                     |
| `cancelUrl`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | URL to redirect the customer to if payment is cancelled.                                      |
| `paymentExpiresAt`                                                                            | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the payment session expires. If omitted, uses the default expiry.                        |