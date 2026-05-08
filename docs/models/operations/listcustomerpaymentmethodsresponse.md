# ListCustomerPaymentMethodsResponse

List of payment methods

## Example Usage

```typescript
import { ListCustomerPaymentMethodsResponse } from "@paygentic/sdk/models/operations";

let value: ListCustomerPaymentMethodsResponse = {
  object: "list",
  data: [
    {
      object: "paymentMethod",
      id: "<id>",
      createdAt: new Date("2025-11-23T08:14:45.787Z"),
    },
  ],
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                   | [operations.ListCustomerPaymentMethodsObject](../../models/operations/listcustomerpaymentmethodsobject.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |
| `data`                                                                                                     | [models.PaymentMethod](../../models/paymentmethod.md)[]                                                    | :heavy_check_mark:                                                                                         | N/A                                                                                                        |