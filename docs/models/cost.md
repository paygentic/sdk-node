# Cost

## Example Usage

```typescript
import { Cost } from "@paygentic/sdk/models";

let value: Cost = {
  id: "<id>",
  type: "metered",
  name: "<value>",
  currency: "Zambian Kwacha",
  unitCost: "<value>",
  productId: "<id>",
  merchantId: "<id>",
  createdAt: new Date("2026-06-08T10:24:09.190Z"),
  updatedAt: new Date("2025-04-03T01:26:14.191Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a cost                                                                  |
| `object`                                                                                      | [models.CostObject](../models/costobject.md)                                                  | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.CostType](../models/costtype.md)                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `unitCost`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal as string to avoid floating point precision loss.                                     |
| `unit`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `aggregation`                                                                                 | [models.CostAggregation](../models/costaggregation.md)                                        | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `eventType`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `valueProperty`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `groupBy`                                                                                     | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `productId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a product                                                               |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `deletedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Soft-delete timestamp. Always null for active costs returned by the API.                      |