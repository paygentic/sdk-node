# GenerateScheduleInvoicesResponse

Staged invoices generated

## Example Usage

```typescript
import { GenerateScheduleInvoicesResponse } from "@paygentic/sdk/models/operations";

let value: GenerateScheduleInvoicesResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      object: "schedule_invoice",
      orderId: "<id>",
      billingScheduleId: "<id>",
      merchantId: "<id>",
      periodStart: new Date("2025-10-02T11:20:52.161Z"),
      periodEnd: new Date("2025-08-07T12:02:36.384Z"),
      dueDate: new Date("2024-08-15T16:42:48.404Z"),
      amount: "362.89",
      status: "cancelled",
      lineItems: [],
      createdAt: new Date("2024-03-23T20:55:03.431Z"),
      updatedAt: new Date("2024-08-15T22:35:22.106Z"),
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

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `object`                                                                                               | [operations.GenerateScheduleInvoicesObject](../../models/operations/generatescheduleinvoicesobject.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `data`                                                                                                 | [models.ScheduleInvoice](../../models/scheduleinvoice.md)[]                                            | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `pagination`                                                                                           | [models.OffsetPagination](../../models/offsetpagination.md)                                            | :heavy_check_mark:                                                                                     | Offset-based pagination response.                                                                      |