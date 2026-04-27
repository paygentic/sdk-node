# CostReportResponse

## Example Usage

```typescript
import { CostReportResponse } from "@paygentic/sdk/models";

let value: CostReportResponse = {
  currency: "Dalasi",
  period: {
    from: new Date("2026-11-03T07:21:44.302Z"),
    to: new Date("2026-07-07T05:23:51.187Z"),
  },
  groupBy: "<value>",
  totalCost: 5504.46,
  totalQuantity: 122.24,
  groups: [],
  timeSeries: [
    {
      windowStart: new Date("2026-08-05T15:26:30.821Z"),
      windowEnd: new Date("2024-09-13T01:19:10.314Z"),
      groups: {
        "key": 2937.19,
      },
    },
  ],
  availableDimensions: [],
  pagination: {
    total: 29030,
    limit: 830242,
    offset: 658657,
  },
};
```

## Fields

| Field                                                                                                                                              | Type                                                                                                                                               | Required                                                                                                                                           | Description                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                                                           | [models.CostReportResponseObject](../models/costreportresponseobject.md)                                                                           | :heavy_minus_sign:                                                                                                                                 | N/A                                                                                                                                                |
| `currency`                                                                                                                                         | *string*                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | ISO 4217 currency code for all monetary values in this response.                                                                                   |
| `period`                                                                                                                                           | [models.Period](../models/period.md)                                                                                                               | :heavy_check_mark:                                                                                                                                 | N/A                                                                                                                                                |
| `groupBy`                                                                                                                                          | *string*                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | The active grouping dimension (e.g. 'cost', 'customer', or a dynamic dimension key).                                                               |
| `totalCost`                                                                                                                                        | *number*                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | Sum of cost across all groups (not just top N).                                                                                                    |
| `totalQuantity`                                                                                                                                    | *number*                                                                                                                                           | :heavy_check_mark:                                                                                                                                 | Sum of quantity across all groups.                                                                                                                 |
| `groups`                                                                                                                                           | [models.CostReportGroup](../models/costreportgroup.md)[]                                                                                           | :heavy_check_mark:                                                                                                                                 | Top N groups plus an 'Other' bucket aggregating the remainder.                                                                                     |
| `timeSeries`                                                                                                                                       | [models.CostReportTimeSeries](../models/costreporttimeseries.md)[]                                                                                 | :heavy_check_mark:                                                                                                                                 | Time-bucketed breakdown per group. Keys in each window's 'groups' object correspond to CostReportGroup.key. The 'Other' bucket key is '__other__'. |
| `availableDimensions`                                                                                                                              | *string*[]                                                                                                                                         | :heavy_check_mark:                                                                                                                                 | Dimension keys available for further drill-down (populated when a single cost is filtered).                                                        |
| `warnings`                                                                                                                                         | *string*[]                                                                                                                                         | :heavy_minus_sign:                                                                                                                                 | Non-fatal warnings, e.g. costs that could not be queried.                                                                                          |
| `pagination`                                                                                                                                       | [models.Pagination](../models/pagination.md)                                                                                                       | :heavy_check_mark:                                                                                                                                 | N/A                                                                                                                                                |