# UpdateCostRequestBody

## Example Usage

```typescript
import { UpdateCostRequestBody } from "@paygentic/sdk/models/operations";

let value: UpdateCostRequestBody = {};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `name`                                                                               | *string*                                                                             | :heavy_minus_sign:                                                                   | Updated name for the cost.                                                           |
| `unitCost`                                                                           | *number*                                                                             | :heavy_minus_sign:                                                                   | Updated unit cost.                                                                   |
| `currency`                                                                           | *string*                                                                             | :heavy_minus_sign:                                                                   | Updated ISO 4217 currency code.                                                      |
| `unit`                                                                               | *string*                                                                             | :heavy_minus_sign:                                                                   | Updated unit label (metered costs only).                                             |
| `aggregation`                                                                        | [operations.UpdateCostAggregation](../../models/operations/updatecostaggregation.md) | :heavy_minus_sign:                                                                   | Updated aggregation method (metered costs only).                                     |
| `eventType`                                                                          | *string*                                                                             | :heavy_minus_sign:                                                                   | Updated CloudEvents type (metered costs only).                                       |
| `valueProperty`                                                                      | *string*                                                                             | :heavy_minus_sign:                                                                   | Updated JSONPath for value extraction (metered costs only).                          |
| `groupBy`                                                                            | Record<string, *string*>                                                             | :heavy_minus_sign:                                                                   | Updated group-by dimension map (metered costs only).                                 |