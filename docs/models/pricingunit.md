# PricingUnit

## Example Usage

```typescript
import { PricingUnit } from "@paygentic/sdk/models";

let value: PricingUnit = {
  id: "<id>",
  merchantId: "<id>",
  identifier: "<value>",
  displayName: "Crawford_Fay",
  shortName: "<value>",
  conversionRate: "<value>",
  currency: "Tenge",
  createdAt: new Date("2026-03-24T22:37:20.351Z"),
  updatedAt: new Date("2026-03-29T06:56:05.499Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a pricing unit                                                          |
| `object`                                                                                      | [models.PricingUnitObject](../models/pricingunitobject.md)                                    | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `identifier`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `displayName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `shortName`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `conversionRate`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Rate converting one credit to the invoicing currency ($/credit), as a decimal string.         |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |