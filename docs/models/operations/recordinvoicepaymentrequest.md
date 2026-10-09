# RecordInvoicePaymentRequest

## Example Usage

```typescript
import { RecordInvoicePaymentRequest } from "@paygentic/sdk/models/operations";

let value: RecordInvoicePaymentRequest = {
  id: "<id>",
  requestBody: {
    method: "out_of_band",
  },
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                     | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The invoice ID                                                                                           |
| `requestBody`                                                                                            | [operations.RecordInvoicePaymentRequestBody](../../models/operations/recordinvoicepaymentrequestbody.md) | :heavy_check_mark:                                                                                       | N/A                                                                                                      |