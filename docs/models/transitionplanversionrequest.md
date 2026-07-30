# TransitionPlanVersionRequest

Sets this version as the plan's default.

## Example Usage

```typescript
import { TransitionPlanVersionRequest } from "@paygentic/sdk/models";

let value: TransitionPlanVersionRequest = {};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `default`                                                                                           | *boolean*                                                                                           | :heavy_minus_sign:                                                                                  | Set to true to point the plan's default at this version. Idempotent on the already-default version. |