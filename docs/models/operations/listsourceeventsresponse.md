# ListSourceEventsResponse

List of source events

## Example Usage

```typescript
import { ListSourceEventsResponse } from "@paygentic/sdk/models/operations";

let value: ListSourceEventsResponse = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.SourceEvent](../../models/sourceevent.md)[]         | :heavy_minus_sign:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_minus_sign:                                          | Offset-based pagination response.                           |