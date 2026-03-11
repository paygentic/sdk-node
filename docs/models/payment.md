# Payment

## Example Usage

```typescript
import { Payment } from "@paygentic/sdk/models";

let value: Payment = {
  id: "<id>",
  amount: "158.77",
  currency: "CFP Franc",
  status: "pending",
  createdAt: new Date("2024-01-05T21:52:54.990Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique payment identifier (pay_* prefixed).                                                   |
| `object`                                                                                      | [models.PaymentObject](../models/paymentobject.md)                                            | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `amount`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Payment amount in decimal format (e.g. '10.50').                                              |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ISO 4217 currency code (e.g. 'USD').                                                          |
| `paymentUrl`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | URL for the customer to complete the payment.                                                 |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | Customer ID if provided.                                                                      |
| `idempotencyKey`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | Client-provided idempotency key.                                                              |
| `reference`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | Merchant-defined reference for this payment.                                                  |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | Merchant-provided key-value metadata.                                                         |
| `lineItems`                                                                                   | [models.PaymentLineItem](../models/paymentlineitem.md)[]                                      | :heavy_minus_sign:                                                                            | Breakdown of what the customer is being charged for.                                          |
| `status`                                                                                      | [models.PaymentStatus](../models/paymentstatus.md)                                            | :heavy_check_mark:                                                                            | Current status of the payment.                                                                |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the payment expires.                                                                     |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the payment was created.                                                                 |