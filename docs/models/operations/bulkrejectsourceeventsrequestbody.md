# BulkRejectSourceEventsRequestBody

## Example Usage

```typescript
import { BulkRejectSourceEventsRequestBody } from "@paygentic/sdk/models/operations";

let value: BulkRejectSourceEventsRequestBody = {
  eventIds: [
    "<value 1>",
  ],
};
```

## Fields

| Field                   | Type                    | Required                | Description             |
| ----------------------- | ----------------------- | ----------------------- | ----------------------- |
| `eventIds`              | *string*[]              | :heavy_check_mark:      | IDs of events to reject |