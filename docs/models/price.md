# Price

## Example Usage

```typescript
import { Price } from "@paygentic/sdk/models";

let value: Price = {
  id: "<id>",
  createdAt: new Date("2026-09-22T03:53:38.745Z"),
  invoiceDisplayName: "<value>",
  model: "volume",
  paymentTerm: "instant",
  properties: {
    "key": "<value>",
  },
  updatedAt: new Date("2026-05-13T02:36:59.563Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a price                                                                 |
| `object`                                                                                      | [models.PriceObject](../models/priceobject.md)                                                | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `billableMetricId`                                                                            | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `feeId`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | The unique identifier for the fee referred to by this price                                   |
| `billingCadence`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | ISO 8601 duration for billing frequency (e.g., P1M for monthly)                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `invoiceDisplayName`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `model`                                                                                       | [models.PriceModel](../models/pricemodel.md)                                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `paymentTerm`                                                                                 | [models.PricePaymentTerm](../models/pricepaymentterm.md)                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `properties`                                                                                  | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `unitAmount`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `features`                                                                                    | [models.PriceFeature](../models/pricefeature.md)[]                                            | :heavy_minus_sign:                                                                            | Features associated with this price                                                           |