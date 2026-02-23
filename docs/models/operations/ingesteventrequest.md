# IngestEventRequest

## Example Usage

```typescript
import { IngestEventRequest } from "@paygentic/sdk/models/operations";

let value: IngestEventRequest = {
  type: "<value>",
  source: "<value>",
  subject: "<value>",
  data: {
    "key": "<value>",
  },
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `type`                                                                                                                            | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | CloudEvents type. Must match an eventType configured on a BillableMetric.                                                         |
| `source`                                                                                                                          | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | Event source URI identifying the application.                                                                                     |
| `subject`                                                                                                                         | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | Customer or entity ID this event relates to.                                                                                      |
| `namespace`                                                                                                                       | *string*                                                                                                                          | :heavy_minus_sign:                                                                                                                | Organization/merchant ID. Defaults to the authenticated user's organization. Platform users can specify a different organization. |
| `timestamp`                                                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                     | :heavy_minus_sign:                                                                                                                | Event timestamp. Defaults to server time if not provided.                                                                         |
| `idempotencyKey`                                                                                                                  | *string*                                                                                                                          | :heavy_minus_sign:                                                                                                                | User-provided deduplication key. If not provided, a unique key is generated.                                                      |
| `data`                                                                                                                            | Record<string, *any*>                                                                                                             | :heavy_check_mark:                                                                                                                | Event payload containing the metering data.                                                                                       |