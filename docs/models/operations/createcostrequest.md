# CreateCostRequest

## Example Usage

```typescript
import { CreateCostRequest } from "@paygentic/sdk/models/operations";

let value: CreateCostRequest = {
  type: "metered",
  name: "<value>",
  unitCost: 3684.89,
  currency: "Tunisian Dinar",
  productId: "<id>",
  aggregation: "SUM",
  eventType: "<value>",
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `type`                                                                                               | [operations.CreateCostType](../../models/operations/createcosttype.md)                               | :heavy_check_mark:                                                                                   | The cost type. Only `metered` costs are supported; they track usage via events.                      |
| `name`                                                                                               | *string*                                                                                             | :heavy_check_mark:                                                                                   | Human-readable name for the cost.                                                                    |
| `unitCost`                                                                                           | *number*                                                                                             | :heavy_check_mark:                                                                                   | Cost per unit, multiplied by measured quantity to compute total cost. Must be non-negative.          |
| `currency`                                                                                           | *string*                                                                                             | :heavy_check_mark:                                                                                   | ISO 4217 currency code (e.g. USD, EUR).                                                              |
| `productId`                                                                                          | *string*                                                                                             | :heavy_check_mark:                                                                                   | Unique identifier for a product                                                                      |
| `unit`                                                                                               | *string*                                                                                             | :heavy_minus_sign:                                                                                   | Unit label for metered costs (e.g. 'token', 'request'). Only valid for metered costs.                |
| `aggregation`                                                                                        | [operations.CreateCostAggregation](../../models/operations/createcostaggregation.md)                 | :heavy_check_mark:                                                                                   | Aggregation method for the metered event.                                                            |
| `eventType`                                                                                          | *string*                                                                                             | :heavy_check_mark:                                                                                   | CloudEvents type that identifies the metered event.                                                  |
| `valueProperty`                                                                                      | *string*                                                                                             | :heavy_minus_sign:                                                                                   | JSONPath to extract numeric value from event data. Required for SUM/AVG/MIN/MAX/LATEST aggregations. |
| `groupBy`                                                                                            | Record<string, *string*>                                                                             | :heavy_minus_sign:                                                                                   | Map of dimension name to JSONPath for group-by queries. Only valid for metered costs.                |
| `merchantId`                                                                                         | *string*                                                                                             | :heavy_minus_sign:                                                                                   | Unique identifier for an organization                                                                |