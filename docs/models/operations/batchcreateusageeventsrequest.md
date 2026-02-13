# BatchCreateUsageEventsRequest

## Example Usage

```typescript
import { BatchCreateUsageEventsRequest } from "@paygentic/sdk/models/operations";

let value: BatchCreateUsageEventsRequest = {
  events: [
    {
      customerId: "<id>",
      idempotencyKey: "<value>",
      merchantId: "<id>",
      properties: [],
      timestamp: new Date("2026-10-05T17:12:26.774Z"),
    },
  ],
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `events`                                                                    | [models.CreateUsageEventRequest](../../models/createusageeventrequest.md)[] | :heavy_check_mark:                                                          | N/A                                                                         |