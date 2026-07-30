# ListBillingSchedulesResponse

List of billing schedules

## Example Usage

```typescript
import { ListBillingSchedulesResponse } from "@paygentic/sdk/models/operations";

let value: ListBillingSchedulesResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      object: "billing_schedule",
      merchantId: "<id>",
      status: "draft",
      startDate: new Date("2024-04-10T11:06:29.482Z"),
      endDate: new Date("2025-09-02T07:29:11.129Z"),
      billingAnchor: new Date("2026-02-04T13:32:16.097Z"),
      alignmentPolicy: "anchor",
      prorationPolicy: "daily",
      periodPreset: "custom",
      customPeriodWindows: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      metadata: {
        "key": "<value>",
        "key1": "<value>",
      },
      createdAt: new Date("2024-08-02T17:12:55.853Z"),
      updatedAt: new Date("2024-08-24T22:49:32.970Z"),
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

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `object`                                                                                       | [operations.ListBillingSchedulesObject](../../models/operations/listbillingschedulesobject.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `data`                                                                                         | [models.SchemasBillingSchedule](../../models/schemasbillingschedule.md)[]                      | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `pagination`                                                                                   | [models.OffsetPagination](../../models/offsetpagination.md)                                    | :heavy_check_mark:                                                                             | Offset-based pagination response.                                                              |