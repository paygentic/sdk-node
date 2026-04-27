# CostReportGroup

## Example Usage

```typescript
import { CostReportGroup } from "@paygentic/sdk/models";

let value: CostReportGroup = {
  key: "<key>",
  label: "<value>",
  totalCost: 3792.46,
  totalQuantity: 2932.24,
  percentOfTotal: 7943.34,
  isOther: true,
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `key`                                                                                                         | *string*                                                                                                      | :heavy_check_mark:                                                                                            | Group identifier (cost ID, customer ID, or dimension value). '__other__' for the aggregated remainder bucket. |
| `label`                                                                                                       | *string*                                                                                                      | :heavy_check_mark:                                                                                            | Human-readable display name for the group.                                                                    |
| `totalCost`                                                                                                   | *number*                                                                                                      | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `totalQuantity`                                                                                               | *number*                                                                                                      | :heavy_check_mark:                                                                                            | N/A                                                                                                           |
| `unit`                                                                                                        | *string*                                                                                                      | :heavy_minus_sign:                                                                                            | Unit label for the quantity (e.g. 'token', 'request').                                                        |
| `percentOfTotal`                                                                                              | *number*                                                                                                      | :heavy_check_mark:                                                                                            | This group's share of total cost, 0–100.                                                                      |
| `priorPeriod`                                                                                                 | [models.PriorPeriod](../models/priorperiod.md)                                                                | :heavy_minus_sign:                                                                                            | Prior-period comparison data. Present only when comparePriorPeriod=true.                                      |
| `isOther`                                                                                                     | *boolean*                                                                                                     | :heavy_check_mark:                                                                                            | True for the aggregated 'Other' bucket.                                                                       |