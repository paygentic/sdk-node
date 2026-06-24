# VoidInvoiceRefundRequest

## Example Usage

```typescript
import { VoidInvoiceRefundRequest } from "@paygentic/sdk/models/operations";

let value: VoidInvoiceRefundRequest = {
  id: "<id>",
  refundId: "<id>",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `id`                                                                                               | *string*                                                                                           | :heavy_check_mark:                                                                                 | The invoice ID                                                                                     |
| `refundId`                                                                                         | *string*                                                                                           | :heavy_check_mark:                                                                                 | The refund (credit note) ID                                                                        |
| `requestBody`                                                                                      | [operations.VoidInvoiceRefundRequestBody](../../models/operations/voidinvoicerefundrequestbody.md) | :heavy_minus_sign:                                                                                 | N/A                                                                                                |