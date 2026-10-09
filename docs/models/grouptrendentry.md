# GroupTrendEntry

## Example Usage

```typescript
import { GroupTrendEntry } from "@paygentic/sdk/models";

let value: GroupTrendEntry = {
  groupKey: "<value>",
  groupLabel: "<value>",
  revenue: "<value>",
  issuedInvoices: "<value>",
};
```

## Fields

| Field                                                                                                                                                        | Type                                                                                                                                                         | Required                                                                                                                                                     | Description                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `groupKey`                                                                                                                                                   | *string*                                                                                                                                                     | :heavy_check_mark:                                                                                                                                           | Unique identifier for the group (e.g. plan ID, or 'other')                                                                                                   |
| `groupLabel`                                                                                                                                                 | *string*                                                                                                                                                     | :heavy_check_mark:                                                                                                                                           | Human-readable label for the group (e.g. plan name)                                                                                                          |
| `revenue`                                                                                                                                                    | *string*                                                                                                                                                     | :heavy_check_mark:                                                                                                                                           | Revenue for this group in this bucket, computed exactly as netRevenue. A group outside the top N, or with only a refund in the window, counts under 'other'. |
| `issuedInvoices`                                                                                                                                             | *string*                                                                                                                                                     | :heavy_check_mark:                                                                                                                                           | Total issued invoice amount in dollars for this group in this bucket, excluding tax, before refunds                                                          |