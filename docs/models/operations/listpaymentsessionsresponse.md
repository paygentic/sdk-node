# ListPaymentSessionsResponse

List of payment sessions

## Example Usage

```typescript
import { ListPaymentSessionsResponse } from "@paygentic/sdk/models/operations";

let value: ListPaymentSessionsResponse = {
  object: "list",
  data: [
    {
      object: "payment_session",
      id: "<id>",
      entityType: "<value>",
      entityId: "<id>",
      amount: "564.55",
      currency: "Quetzal",
      status: "completed",
      createdAt: new Date("2024-03-13T01:03:12.484Z"),
      updatedAt: new Date("2024-12-07T10:55:16.497Z"),
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `object`                                                                                     | [operations.ListPaymentSessionsObject](../../models/operations/listpaymentsessionsobject.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `data`                                                                                       | [models.SchemasPaymentSession](../../models/schemaspaymentsession.md)[]                      | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `pagination`                                                                                 | [models.OffsetPagination](../../models/offsetpagination.md)                                  | :heavy_check_mark:                                                                           | Offset-based pagination response.                                                            |