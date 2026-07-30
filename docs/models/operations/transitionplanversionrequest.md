# TransitionPlanVersionRequest

## Example Usage

```typescript
import { TransitionPlanVersionRequest } from "@paygentic/sdk/models/operations";

let value: TransitionPlanVersionRequest = {
  id: "<id>",
  versionNumber: 178959,
  transitionPlanVersionRequest: {},
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | N/A                                                                                 |
| `versionNumber`                                                                     | *number*                                                                            | :heavy_check_mark:                                                                  | The version number within the plan (1-based).                                       |
| `transitionPlanVersionRequest`                                                      | [models.TransitionPlanVersionRequest](../../models/transitionplanversionrequest.md) | :heavy_check_mark:                                                                  | N/A                                                                                 |