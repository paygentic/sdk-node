# RecordInvoicePaymentRequestBody

## Example Usage

```typescript
import { RecordInvoicePaymentRequestBody } from "@paygentic/sdk/models/operations";

let value: RecordInvoicePaymentRequestBody = {
  method: "hosted_link",
};
```

## Fields

| Field                                                                                                                                                      | Type                                                                                                                                                       | Required                                                                                                                                                   | Description                                                                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `method`                                                                                                                                                   | [models.InvoicePaymentMethod](../../models/invoicepaymentmethod.md)                                                                                        | :heavy_check_mark:                                                                                                                                         | How an invoice payment is settled.                                                                                                                         |
| `reason`                                                                                                                                                   | *string*                                                                                                                                                   | :heavy_minus_sign:                                                                                                                                         | Optional note for `out_of_band` that describes how you received the payment (for example, 'Wire transfer received 2026-03-25'). Ignored for `hosted_link`. |