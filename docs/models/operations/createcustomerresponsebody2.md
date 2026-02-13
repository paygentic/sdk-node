# CreateCustomerResponseBody2

Customer created successfully

## Example Usage

```typescript
import { CreateCustomerResponseBody2 } from "@paygentic/sdk/models/operations";

let value: CreateCustomerResponseBody2 = {
  customerId: "<id>",
  validTaxAddress: {
    valid: false,
  },
};
```

## Fields

| Field                                                                                                                                                                                                       | Type                                                                                                                                                                                                        | Required                                                                                                                                                                                                    | Description                                                                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `customerId`                                                                                                                                                                                                | *string*                                                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                                                          | N/A                                                                                                                                                                                                         |
| `validTaxAddress`                                                                                                                                                                                           | [models.ValidTaxAddress](../../models/validtaxaddress.md)                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                          | Indicates whether the consumer address is valid for tax calculation when using Paygentic Tax. If valid=false, tax calculation will be skipped and internal invoice flow with default tax rate will be used. |