# GetEntitlementGrantRequest

## Example Usage

```typescript
import { GetEntitlementGrantRequest } from "@paygentic/sdk/models/operations";

let value: GetEntitlementGrantRequest = {
  entitlementId: "<id>",
  grantId: "<id>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `entitlementId`                           | *string*                                  | :heavy_check_mark:                        | The unique identifier of the entitlement. |
| `grantId`                                 | *string*                                  | :heavy_check_mark:                        | The unique identifier of the grant.       |