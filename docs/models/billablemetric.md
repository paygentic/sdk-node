# BillableMetric

## Example Usage

```typescript
import { BillableMetric } from "@paygentic/sdk/models";

let value: BillableMetric = {
  id: "<id>",
  aggregation: "UNIQUE_COUNT",
  createdAt: new Date("2025-07-20T23:56:51.292Z"),
  description: "sparse vicinity icebreaker inure gadzooks hunger overload",
  merchantId: "<id>",
  name: "<value>",
  productId: "<id>",
  unit: "sievert",
  updatedAt: new Date("2025-07-03T17:54:44.325Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a billable metric                                                       |
| `object`                                                                                      | [models.BillableMetricObject](../models/billablemetricobject.md)                              | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `aggregation`                                                                                 | [models.Aggregation](../models/aggregation.md)                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `productId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a product                                                               |
| `unit`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `eventType`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `valueProperty`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `groupBy`                                                                                     | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `eventFrom`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |