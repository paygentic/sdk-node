# BatchUsageEventResponse

## Example Usage

```typescript
import { BatchUsageEventResponse } from "@paygentic/sdk/models";

let value: BatchUsageEventResponse = {
  object: "batchUsageEvents",
  failed: [
    {
      error: "<value>",
      idempotencyKey: "<value>",
      index: 650433,
    },
  ],
  successful: [
    {
      id: "<id>",
      object: "usageEvent",
      createdAt: new Date("2024-10-30T21:03:45.392Z"),
      customerId: "<id>",
      merchantId: "<id>",
      properties: [],
      subscriptionId: "<id>",
      timestamp: new Date("2025-05-31T23:05:22.507Z"),
    },
  ],
  summary: {
    failed: 634036,
    successful: 261798,
    total: 229283,
  },
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `object`                                                                           | [models.BatchUsageEventResponseObject](../models/batchusageeventresponseobject.md) | :heavy_check_mark:                                                                 | N/A                                                                                |
| `failed`                                                                           | [models.Failed](../models/failed.md)[]                                             | :heavy_check_mark:                                                                 | Array of events that failed to be created with error details                       |
| `successful`                                                                       | [models.UsageEvent](../models/usageevent.md)[]                                     | :heavy_check_mark:                                                                 | Array of successfully created usage events                                         |
| `summary`                                                                          | [models.Summary](../models/summary.md)                                             | :heavy_check_mark:                                                                 | Summary of batch processing results                                                |