# GetPlanVersionRequest

## Example Usage

```typescript
import { GetPlanVersionRequest } from "@paygentic/sdk/models/operations";

let value: GetPlanVersionRequest = {
  id: "<id>",
  versionNumber: 971036,
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `id`                                          | *string*                                      | :heavy_check_mark:                            | N/A                                           |
| `versionNumber`                               | *number*                                      | :heavy_check_mark:                            | The version number within the plan (1-based). |