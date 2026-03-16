# RevenueSummaryResponse

## Example Usage

```typescript
import { RevenueSummaryResponse } from "@paygentic/sdk/models";

let value: RevenueSummaryResponse = {
  object: "revenue_summary",
  netRevenue: "<value>",
  invoices: {
    issued: {
      count: 282125,
      amount: "674.64",
    },
    outstanding: {
      count: 136097,
      amount: "969.47",
    },
    paid: {
      count: 679467,
      amount: "317.76",
    },
    writtenOff: {
      count: 94548,
      amount: "637.88",
    },
  },
  payments: {
    completedCount: 274656,
    completedAmount: "<value>",
    pendingCount: 158750,
    pendingAmount: "<value>",
    expiredCount: 27548,
    expiredAmount: "<value>",
  },
  trend: [],
};
```

## Fields

| Field                                                                         | Type                                                                          | Required                                                                      | Description                                                                   |
| ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| `object`                                                                      | *"revenue_summary"*                                                           | :heavy_check_mark:                                                            | Object type identifier                                                        |
| `netRevenue`                                                                  | *string*                                                                      | :heavy_check_mark:                                                            | Net collected revenue in dollars (paid invoices + completed payments)         |
| `invoices`                                                                    | [models.InvoiceSummary](../models/invoicesummary.md)                          | :heavy_check_mark:                                                            | N/A                                                                           |
| `payments`                                                                    | [models.PaymentSummary](../models/paymentsummary.md)                          | :heavy_check_mark:                                                            | N/A                                                                           |
| `trend`                                                                       | [models.RevenueTrendBucket](../models/revenuetrendbucket.md)[]                | :heavy_check_mark:                                                            | Time-bucketed revenue trend data                                              |
| `groupBreakdown`                                                              | [models.GroupInvoiceSummary](../models/groupinvoicesummary.md)[]              | :heavy_minus_sign:                                                            | Invoice breakdown by group dimension (only present when groupBy is specified) |