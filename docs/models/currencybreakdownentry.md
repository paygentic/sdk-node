# CurrencyBreakdownEntry

## Example Usage

```typescript
import { CurrencyBreakdownEntry } from "@paygentic/sdk/models";

let value: CurrencyBreakdownEntry = {
  currency: "Uganda Shilling",
  netRevenue: "<value>",
  invoices: {
    issued: {
      count: 366546,
      amount: "774.49",
    },
    outstanding: {
      count: 965637,
      amount: "159.49",
    },
    paid: {
      count: 140409,
      amount: "166.95",
    },
    writtenOff: {
      count: 466682,
      amount: "143.09",
    },
  },
  payments: {
    completedCount: 343773,
    completedAmount: "<value>",
    pendingCount: 115435,
    pendingAmount: "<value>",
    expiredCount: 38595,
    expiredAmount: "<value>",
  },
  trend: [
    {
      timestamp: new Date("2024-12-31T23:02:21.599Z"),
      issuedInvoices: "<value>",
      writtenOffInvoices: "<value>",
      completedPayments: "<value>",
    },
  ],
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `currency`                                                                                | *string*                                                                                  | :heavy_check_mark:                                                                        | ISO 4217 currency code (uppercase, e.g. USD, EUR, GBP)                                    |
| `netRevenue`                                                                              | *string*                                                                                  | :heavy_check_mark:                                                                        | Net collected revenue in dollars for this currency (issued invoices + completed payments) |
| `invoices`                                                                                | [models.InvoiceSummary](../models/invoicesummary.md)                                      | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `payments`                                                                                | [models.PaymentSummary](../models/paymentsummary.md)                                      | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `trend`                                                                                   | [models.RevenueTrendBucket](../models/revenuetrendbucket.md)[]                            | :heavy_check_mark:                                                                        | Time-bucketed revenue trend data for this currency                                        |