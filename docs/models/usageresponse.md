# UsageResponse

## Example Usage

```typescript
import { UsageResponse } from "@paygentic/sdk/models";

let value: UsageResponse = {
  billableMetricId: "<id>",
  totalValue: 7636.41,
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `object`                                                          | [models.UsageResponseObject](../models/usageresponseobject.md)    | :heavy_minus_sign:                                                | N/A                                                               |
| `billableMetricId`                                                | *string*                                                          | :heavy_check_mark:                                                | Unique identifier for a billable metric                           |
| `totalValue`                                                      | *number*                                                          | :heavy_check_mark:                                                | Total aggregated value across the query window                    |
| `windowedValues`                                                  | [models.WindowedValue](../models/windowedvalue.md)[]              | :heavy_minus_sign:                                                | Time-bucketed values. Only present when windowSize is specified.  |
| `groupedValues`                                                   | [models.GroupedValue](../models/groupedvalue.md)[]                | :heavy_minus_sign:                                                | Dimension-grouped values. Only present when groupBy is specified. |