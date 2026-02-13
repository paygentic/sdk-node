# RevenueTimeSeriesResponse

## Example Usage

```typescript
import { RevenueTimeSeriesResponse } from "@paygentic/sdk/models";

let value: RevenueTimeSeriesResponse = {
  object: "revenue_time_series",
  buckets: [],
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `object`                                                     | *"revenue_time_series"*                                      | :heavy_check_mark:                                           | Object type identifier                                       |
| `buckets`                                                    | [models.RevenueTimeBucket](../models/revenuetimebucket.md)[] | :heavy_check_mark:                                           | Time-bucketed revenue data                                   |