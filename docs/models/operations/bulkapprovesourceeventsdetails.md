# BulkApproveSourceEventsDetails

## Example Usage

```typescript
import { BulkApproveSourceEventsDetails } from "@paygentic/sdk/models/operations";

let value: BulkApproveSourceEventsDetails = {};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `processed`                                              | *string*[]                                               | :heavy_minus_sign:                                       | IDs of successfully processed events                     |
| `failed`                                                 | [operations.Failed](../../models/operations/failed.md)[] | :heavy_minus_sign:                                       | Failed events with error messages                        |