# GroupInvoiceSummary

## Example Usage

```typescript
import { GroupInvoiceSummary } from "@paygentic/sdk/models";

let value: GroupInvoiceSummary = {
  groupKey: "<value>",
  groupLabel: "<value>",
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
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `groupKey`                                                           | *string*                                                             | :heavy_check_mark:                                                   | Unique identifier for the group (e.g. plan ID, or 'other')           |
| `groupLabel`                                                         | *string*                                                             | :heavy_check_mark:                                                   | Human-readable label for the group (e.g. plan name)                  |
| `outstanding`                                                        | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `paid`                                                               | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `writtenOff`                                                         | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |