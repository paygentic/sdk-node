# ProfitabilitySummaryResponse

## Example Usage

```typescript
import { ProfitabilitySummaryResponse } from "@paygentic/sdk/models";

let value: ProfitabilitySummaryResponse = {
  object: "profitability_summary",
  currency: "Bermudian Dollar (customarily known as Bermuda Dollar)",
  rows: [
    {
      customerId: "<id>",
      customerName: "<value>",
      netRevenue: "<value>",
      totalCost: "<value>",
      profit: "<value>",
      marginPct: null,
      trend: {
        values: [],
        periodChange: 8182.99,
      },
    },
  ],
};
```

## Fields

| Field                                                                                                                            | Type                                                                                                                             | Required                                                                                                                         | Description                                                                                                                      |
| -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                                         | *"profitability_summary"*                                                                                                        | :heavy_check_mark:                                                                                                               | Object type identifier                                                                                                           |
| `currency`                                                                                                                       | *string*                                                                                                                         | :heavy_check_mark:                                                                                                               | ISO 4217 currency code applied to revenue and cost values                                                                        |
| `rows`                                                                                                                           | [models.ProfitabilityRow](../models/profitabilityrow.md)[]                                                                       | :heavy_check_mark:                                                                                                               | Top-N customer rows by profit descending, optionally followed by a single 'Other' row when more than topN customers contributed. |
| `warnings`                                                                                                                       | *string*[]                                                                                                                       | :heavy_minus_sign:                                                                                                               | Non-fatal warnings collected during cost discovery (e.g. an individual cost query failed). Empty array on a clean run.           |