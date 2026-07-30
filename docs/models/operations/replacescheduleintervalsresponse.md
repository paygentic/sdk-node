# ReplaceScheduleIntervalsResponse

Intervals replaced

## Example Usage

```typescript
import { ReplaceScheduleIntervalsResponse } from "@paygentic/sdk/models/operations";

let value: ReplaceScheduleIntervalsResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      object: "schedule_interval",
      scheduleId: "<id>",
      baseQuantity: "<value>",
      quantityTransitions: [],
      billingCadence: "<value>",
      billingMode: "arrears",
      startDate: new Date("2026-01-11T08:11:01.394Z"),
      endDate: new Date("2024-05-21T20:59:18.871Z"),
      metadata: {
        "key": "<value>",
      },
      createdAt: new Date("2026-05-21T13:29:09.064Z"),
      updatedAt: new Date("2025-08-02T06:48:56.749Z"),
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
| `object`                                                                                               | [operations.ReplaceScheduleIntervalsObject](../../models/operations/replacescheduleintervalsobject.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `data`                                                                                                 | [models.ScheduleInterval](../../models/scheduleinterval.md)[]                                          | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `pagination`                                                                                           | [models.OffsetPagination](../../models/offsetpagination.md)                                            | :heavy_check_mark:                                                                                     | Offset-based pagination response.                                                                      |