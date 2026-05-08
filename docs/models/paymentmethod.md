# PaymentMethod

## Example Usage

```typescript
import { PaymentMethod } from "@paygentic/sdk/models";

let value: PaymentMethod = {
  object: "paymentMethod",
  id: "<id>",
  createdAt: new Date("2026-09-01T00:13:53.086Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.PaymentMethodObject](../models/paymentmethodobject.md)                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Payment method identifier.                                                                    |
| `type`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | Payment method type (e.g. `card`, `sepa_debit`).                                              |
| `brand`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `last4`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `expMonth`                                                                                    | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `expYear`                                                                                     | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |