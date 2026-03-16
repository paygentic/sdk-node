# InvoiceCategorySummary

## Example Usage

```typescript
import { InvoiceCategorySummary } from "@paygentic/sdk/models";

let value: InvoiceCategorySummary = {
  count: 600483,
  amount: "807.57",
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `count`                                              | *number*                                             | :heavy_check_mark:                                   | Number of invoices in this category                  |
| `amount`                                             | *string*                                             | :heavy_check_mark:                                   | Total amount of invoices in this category in dollars |