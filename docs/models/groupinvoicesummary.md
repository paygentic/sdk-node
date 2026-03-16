# GroupInvoiceSummary

## Example Usage

```typescript
import { GroupInvoiceSummary } from "@paygentic/sdk/models";

let value: GroupInvoiceSummary = {
  groupKey: "<value>",
  groupLabel: "<value>",
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