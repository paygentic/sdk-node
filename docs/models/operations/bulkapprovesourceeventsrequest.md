# BulkApproveSourceEventsRequest

## Example Usage

```typescript
import { BulkApproveSourceEventsRequest } from "@paygentic/sdk/models/operations";

let value: BulkApproveSourceEventsRequest = {
  id: "<id>",
  requestBody: {
    eventIds: [
      "<value 1>",
      "<value 2>",
      "<value 3>",
    ],
  },
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                           | *string*                                                                                                       | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `requestBody`                                                                                                  | [operations.BulkApproveSourceEventsRequestBody](../../models/operations/bulkapprovesourceeventsrequestbody.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |