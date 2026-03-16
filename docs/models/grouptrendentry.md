# GroupTrendEntry

## Example Usage

```typescript
import { GroupTrendEntry } from "@paygentic/sdk/models";

let value: GroupTrendEntry = {
  groupKey: "<value>",
  groupLabel: "<value>",
  issuedInvoices: "<value>",
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `groupKey`                                                           | *string*                                                             | :heavy_check_mark:                                                   | Unique identifier for the group (e.g. plan ID, or 'other')           |
| `groupLabel`                                                         | *string*                                                             | :heavy_check_mark:                                                   | Human-readable label for the group (e.g. plan name)                  |
| `issuedInvoices`                                                     | *string*                                                             | :heavy_check_mark:                                                   | Total issued invoice amount in dollars for this group in this bucket |