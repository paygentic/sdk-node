# InvoiceRefundList

## Example Usage

```typescript
import { InvoiceRefundList } from "@paygentic/sdk/models";

let value: InvoiceRefundList = {
  object: "list",
  data: [
    {
      object: "invoice_refund",
      id: "<id>",
      invoiceId: "<id>",
      merchantId: "<id>",
      amount: "315.62",
      taxAmount: "<value>",
      total: "<value>",
      currency: "Turkish Lira",
      status: "VOIDED",
      externalCreditNoteId: "<id>",
      createdAt: new Date("2025-07-11T11:10:54.969Z"),
    },
  ],
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `object`                                                               | [models.InvoiceRefundListObject](../models/invoicerefundlistobject.md) | :heavy_check_mark:                                                     | The object type                                                        |
| `data`                                                                 | [models.InvoiceRefund](../models/invoicerefund.md)[]                   | :heavy_check_mark:                                                     | The refunds for this invoice                                           |