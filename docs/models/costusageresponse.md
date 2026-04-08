# CostUsageResponse

## Example Usage

```typescript
import { CostUsageResponse } from "@paygentic/sdk/models";

let value: CostUsageResponse = {
  id: "<id>",
  name: "<value>",
  type: "metered",
  currency: "Seychelles Rupee",
  totalCost: 8442.78,
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `object`                                                                     | [models.CostUsageResponseObject](../models/costusageresponseobject.md)       | :heavy_minus_sign:                                                           | N/A                                                                          |
| `id`                                                                         | *string*                                                                     | :heavy_check_mark:                                                           | Unique identifier for a cost                                                 |
| `name`                                                                       | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `type`                                                                       | [models.CostUsageResponseType](../models/costusageresponsetype.md)           | :heavy_check_mark:                                                           | N/A                                                                          |
| `currency`                                                                   | *string*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `eventType`                                                                  | *string*                                                                     | :heavy_minus_sign:                                                           | CloudEvents type for metered costs.                                          |
| `totalCost`                                                                  | *number*                                                                     | :heavy_check_mark:                                                           | Total cost for the query window. Null if usage data could not be computed.   |
| `totalQuantity`                                                              | *number*                                                                     | :heavy_minus_sign:                                                           | Total usage quantity (metered costs only). Null when usage was not computed. |
| `groups`                                                                     | [models.Group](../models/group.md)[]                                         | :heavy_minus_sign:                                                           | Per-group breakdown (present when groupBy is specified).                     |
| `timeSeries`                                                                 | [models.TimeSery](../models/timesery.md)[]                                   | :heavy_minus_sign:                                                           | Time-series breakdown (present when window is specified).                    |