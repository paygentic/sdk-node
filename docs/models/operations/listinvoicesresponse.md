# ListInvoicesResponse

List of invoices

## Example Usage

```typescript
import { ListInvoicesResponse } from "@paygentic/sdk/models/operations";

let value: ListInvoicesResponse = {
  object: "list",
  data: [],
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [operations.ListInvoicesObject](../../models/operations/listinvoicesobject.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `data`                                                                         | [models.Invoice](../../models/invoice.md)[]                                    | :heavy_check_mark:                                                             | N/A                                                                            |