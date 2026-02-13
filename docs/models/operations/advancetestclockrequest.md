# AdvanceTestClockRequest

## Example Usage

```typescript
import { AdvanceTestClockRequest } from "@paygentic/sdk/models/operations";

let value: AdvanceTestClockRequest = {
  id: "<id>",
  requestBody: {
    advanceBy: "<value>",
  },
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `id`                                     | *string*                                 | :heavy_check_mark:                       | Test clock ID                            |
| `requestBody`                            | *operations.AdvanceTestClockRequestBody* | :heavy_check_mark:                       | N/A                                      |