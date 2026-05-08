# ListInvoicesResponse

List of invoices

## Example Usage

```typescript
import { ListInvoicesResponse } from "@paygentic/sdk/models/operations";

let value: ListInvoicesResponse = {
  object: "list",
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [operations.ListInvoicesObject](../../models/operations/listinvoicesobject.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `data`                                                                         | [models.Invoice](../../models/invoice.md)[]                                    | :heavy_check_mark:                                                             | N/A                                                                            |
| `pagination`                                                                   | [models.OffsetPagination](../../models/offsetpagination.md)                    | :heavy_check_mark:                                                             | Offset-based pagination response.                                              |