# ListScheduleIntervalsResponse

List of schedule intervals

## Example Usage

```typescript
import { ListScheduleIntervalsResponse } from "@paygentic/sdk/models/operations";

let value: ListScheduleIntervalsResponse = {
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

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `object`                                                                                         | [operations.ListScheduleIntervalsObject](../../models/operations/listscheduleintervalsobject.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `data`                                                                                           | [models.ScheduleInterval](../../models/scheduleinterval.md)[]                                    | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `pagination`                                                                                     | [models.OffsetPagination](../../models/offsetpagination.md)                                      | :heavy_check_mark:                                                                               | Offset-based pagination response.                                                                |