# ListPaymentSessionsResponse

List of payments

## Example Usage

```typescript
import { ListPaymentSessionsResponse } from "@paygentic/sdk/models/operations";

let value: ListPaymentSessionsResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      amount: "564.55",
      currency: "Quetzal",
      status: "processing",
      createdAt: new Date("2024-03-13T01:03:12.484Z"),
    },
  ],
  pagination: {},
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `object`                                                                                     | [operations.ListPaymentSessionsObject](../../models/operations/listpaymentsessionsobject.md) | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `data`                                                                                       | [models.Payment](../../models/payment.md)[]                                                  | :heavy_check_mark:                                                                           | N/A                                                                                          |
| `pagination`                                                                                 | [models.OffsetPagination](../../models/offsetpagination.md)                                  | :heavy_check_mark:                                                                           | Offset-based pagination response.                                                            |