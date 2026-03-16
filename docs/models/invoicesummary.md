# InvoiceSummary

## Example Usage

```typescript
import { InvoiceSummary } from "@paygentic/sdk/models";

let value: InvoiceSummary = {
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
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `issued`                                                             | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `outstanding`                                                        | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `paid`                                                               | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |
| `writtenOff`                                                         | [models.InvoiceCategorySummary](../models/invoicecategorysummary.md) | :heavy_check_mark:                                                   | N/A                                                                  |