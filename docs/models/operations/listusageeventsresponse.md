# ListUsageEventsResponse

List of usage events

## Example Usage

```typescript
import { ListUsageEventsResponse } from "@paygentic/sdk/models/operations";

let value: ListUsageEventsResponse = {};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `object`                                                                             | [operations.ListUsageEventsObject](../../models/operations/listusageeventsobject.md) | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `data`                                                                               | [models.UsageEvent](../../models/usageevent.md)[]                                    | :heavy_minus_sign:                                                                   | N/A                                                                                  |
| `pagination`                                                                         | [models.OffsetPagination](../../models/offsetpagination.md)                          | :heavy_minus_sign:                                                                   | Offset-based pagination response.                                                    |