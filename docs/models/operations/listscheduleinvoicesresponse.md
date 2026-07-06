# ListScheduleInvoicesResponse

List of staged invoices

## Example Usage

```typescript
import { ListScheduleInvoicesResponse } from "@paygentic/sdk/models/operations";

let value: ListScheduleInvoicesResponse = {
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

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `object`                                                                                       | [operations.ListScheduleInvoicesObject](../../models/operations/listscheduleinvoicesobject.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `data`                                                                                         | [models.ScheduleInvoice](../../models/scheduleinvoice.md)[]                                    | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `pagination`                                                                                   | [models.OffsetPagination](../../models/offsetpagination.md)                                    | :heavy_check_mark:                                                                             | Offset-based pagination response.                                                              |