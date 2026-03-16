# VoidEntitlementGrantRequest

## Example Usage

```typescript
import { VoidEntitlementGrantRequest } from "@paygentic/sdk/models/operations";

let value: VoidEntitlementGrantRequest = {
  entitlementId: "<id>",
  grantId: "<id>",
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `entitlementId`                             | *string*                                    | :heavy_check_mark:                          | The unique identifier of the entitlement.   |
| `grantId`                                   | *string*                                    | :heavy_check_mark:                          | The unique identifier of the grant to void. |