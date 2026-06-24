# InvoiceRefund

## Example Usage

```typescript
import { InvoiceRefund } from "@paygentic/sdk/models";

let value: InvoiceRefund = {
  object: "invoice_refund",
  id: "<id>",
  invoiceId: "<id>",
  merchantId: "<id>",
  amount: "111.70",
  taxAmount: "<value>",
  total: "<value>",
  currency: "Vatu",
  status: "ISSUED",
  externalCreditNoteId: "<id>",
  createdAt: new Date("2025-08-29T22:04:37.192Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.InvoiceRefundObject](../models/invoicerefundobject.md)                                | :heavy_check_mark:                                                                            | The object type                                                                               |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | The credit note ID (crn_*)                                                                    |
| `invoiceId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The invoice this refund credits                                                               |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The merchant that owns the invoice                                                            |
| `amount`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Refunded subtotal (pre-tax) in decimal dollars                                                |
| `taxAmount`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Reversed tax in decimal dollars                                                               |
| `total`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | Total refunded (amount + taxAmount) in decimal dollars                                        |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ISO 4217 currency code                                                                        |
| `status`                                                                                      | [models.InvoiceRefundStatus](../models/invoicerefundstatus.md)                                | :heavy_check_mark:                                                                            | Credit note status                                                                            |
| `externalCreditNoteId`                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | Credit note id in the tax provider                                                            |
| `permalink`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | Public URL to view the credit note document                                                   |
| `pdfUrl`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | Direct PDF download link                                                                      |
| `reason`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | Optional refund reason                                                                        |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the refund was issued                                                                    |
| `voidedAt`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the refund was voided, if applicable                                                     |