# BulkApproveSourceEventsResponse

Bulk approval results

## Example Usage

```typescript
import { BulkApproveSourceEventsResponse } from "@paygentic/sdk/models/operations";

let value: BulkApproveSourceEventsResponse = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `processed`                                                                                            | *number*                                                                                               | :heavy_minus_sign:                                                                                     | Number of successfully approved events                                                                 |
| `failed`                                                                                               | *number*                                                                                               | :heavy_minus_sign:                                                                                     | Number of events that failed to process                                                                |
| `details`                                                                                              | [operations.BulkApproveSourceEventsDetails](../../models/operations/bulkapprovesourceeventsdetails.md) | :heavy_minus_sign:                                                                                     | N/A                                                                                                    |