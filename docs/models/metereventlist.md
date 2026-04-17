# MeterEventList

## Example Usage

```typescript
import { MeterEventList } from "@paygentic/sdk/models";

let value: MeterEventList = {
  billableMetricId: "<id>",
  events: [],
  pagination: {},
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `object`                                                         | [models.MeterEventListObject](../models/metereventlistobject.md) | :heavy_minus_sign:                                               | N/A                                                              |
| `billableMetricId`                                               | *string*                                                         | :heavy_check_mark:                                               | Unique identifier for a billable metric                          |
| `events`                                                         | [models.MeterEvent](../models/meterevent.md)[]                   | :heavy_check_mark:                                               | N/A                                                              |
| `pagination`                                                     | [models.OffsetPagination](../models/offsetpagination.md)         | :heavy_check_mark:                                               | Offset-based pagination response.                                |