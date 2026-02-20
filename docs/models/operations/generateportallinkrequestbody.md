# GeneratePortalLinkRequestBody

## Example Usage

```typescript
import { GeneratePortalLinkRequestBody } from "@paygentic/sdk/models/operations";

let value: GeneratePortalLinkRequestBody = {};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `expiresIn`                                                                                                                       | *string*                                                                                                                          | :heavy_minus_sign:                                                                                                                | Token lifetime as an ISO 8601 duration. Defaults to PT10M (10 minutes). Maximum is P7D (7 days). Examples: PT10M, PT1H, P1D, P7D. |