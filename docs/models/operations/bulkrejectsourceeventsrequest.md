# BulkRejectSourceEventsRequest

## Example Usage

```typescript
import { BulkRejectSourceEventsRequest } from "@paygentic/sdk/models/operations";

let value: BulkRejectSourceEventsRequest = {
  id: "<id>",
  requestBody: {
    eventIds: [
      "<value 1>",
    ],
  },
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                         | *string*                                                                                                     | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `requestBody`                                                                                                | [operations.BulkRejectSourceEventsRequestBody](../../models/operations/bulkrejectsourceeventsrequestbody.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |