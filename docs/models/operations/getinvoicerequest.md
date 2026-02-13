# GetInvoiceRequest

## Example Usage

```typescript
import { GetInvoiceRequest } from "@paygentic/sdk/models/operations";

let value: GetInvoiceRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `id`                                                                    | *string*                                                                | :heavy_check_mark:                                                      | The invoice ID                                                          |
| `expand`                                                                | *string*                                                                | :heavy_minus_sign:                                                      | Comma-separated list of fields to expand. Currently supports: lineItems |
| `lineItemsLimit`                                                        | *number*                                                                | :heavy_minus_sign:                                                      | Page size for line items when expand=lineItems                          |
| `lineItemsPageToken`                                                    | *string*                                                                | :heavy_minus_sign:                                                      | Pagination token for line items when expand=lineItems                   |