# InvoiceSummary

## Example Usage

```typescript
import { InvoiceSummary } from "@paygentic/sdk/models";

let value: InvoiceSummary = {
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
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `issued`                                                             | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `outstanding`                                                        | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `paid`                                                               | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `writtenOff`                                                         | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |