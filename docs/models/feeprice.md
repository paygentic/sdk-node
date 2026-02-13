# FeePrice

The price configuration for a fee within a subscription context.

## Example Usage

```typescript
import { FeePrice } from "@paygentic/sdk/models";

let value: FeePrice = {
  id: "<id>",
  feeId: "<id>",
  model: "standard",
  paymentTerm: "in_arrears",
  invoiceDisplayName: "<value>",
  properties: {
    unitPrice: "<value>",
  },
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `id`                                                           | *string*                                                       | :heavy_check_mark:                                             | The unique identifier of the price.                            |
| `feeId`                                                        | *string*                                                       | :heavy_check_mark:                                             | The unique identifier of the fee.                              |
| `model`                                                        | [models.FeePriceModel](../models/feepricemodel.md)             | :heavy_check_mark:                                             | The pricing model. Fees only support standard pricing.         |
| `paymentTerm`                                                  | [models.FeePricePaymentTerm](../models/feepricepaymentterm.md) | :heavy_check_mark:                                             | When the fee is charged relative to the billing period.        |
| `invoiceDisplayName`                                           | *string*                                                       | :heavy_check_mark:                                             | The name to display on invoices for this fee.                  |
| `properties`                                                   | [models.Properties](../models/properties.md)                   | :heavy_check_mark:                                             | N/A                                                            |
| `taxRate`                                                      | *number*                                                       | :heavy_minus_sign:                                             | The tax rate as a percentage (e.g., 10 for 10%).               |