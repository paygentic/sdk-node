# ProfitabilityRow

## Example Usage

```typescript
import { ProfitabilityRow } from "@paygentic/sdk/models";

let value: ProfitabilityRow = {
  customerId: "<id>",
  customerName: "<value>",
  netRevenue: "<value>",
  totalCost: "<value>",
  profit: "<value>",
  marginPct: "<value>",
  trend: {
    values: [],
    periodChange: 8182.99,
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `customerId`                                                                                             | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Customer ID, or the literal 'other' for the overflow row.                                                |
| `customerName`                                                                                           | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Display name for the row. 'Other' for the overflow row.                                                  |
| `netRevenue`                                                                                             | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Net revenue (paid + outstanding) in unit currency, with two decimals.                                    |
| `totalCost`                                                                                              | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Aggregated cost in unit currency, with two decimals.                                                     |
| `profit`                                                                                                 | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Profit (revenue − cost) in unit currency, with two decimals. May be negative.                            |
| `marginPct`                                                                                              | *string*                                                                                                 | :heavy_check_mark:                                                                                       | Margin percent (profit / revenue × 100), with two decimals. Null when revenue is zero.                   |
| `trend`                                                                                                  | [models.ProfitabilityTrend](../models/profitabilitytrend.md)                                             | :heavy_check_mark:                                                                                       | Per-customer revenue trend over the period. Null for the 'Other' row and when there's insufficient data. |