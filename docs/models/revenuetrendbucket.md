# RevenueTrendBucket

## Example Usage

```typescript
import { RevenueTrendBucket } from "@paygentic/sdk/models";

let value: RevenueTrendBucket = {
  timestamp: new Date("2025-10-23T17:57:00.150Z"),
  issuedInvoices: "<value>",
  writtenOffInvoices: "<value>",
  completedPayments: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `timestamp`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Start time of this bucket                                                                     |
| `issuedInvoices`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Total amount of all invoices issued in this bucket (all statuses, by issuedAt)                |
| `writtenOffInvoices`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Amount of written-off invoices in dollars for this bucket (by writtenOffAt)                   |
| `completedPayments`                                                                           | *string*                                                                                      | :heavy_check_mark:                                                                            | Revenue from completed payments in dollars for this bucket                                    |
| `groupBreakdown`                                                                              | [models.GroupTrendEntry](../models/grouptrendentry.md)[]                                      | :heavy_minus_sign:                                                                            | Per-group trend entries (only present when groupBy is specified)                              |