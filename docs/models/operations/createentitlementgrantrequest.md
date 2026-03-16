# CreateEntitlementGrantRequest

## Example Usage

```typescript
import { CreateEntitlementGrantRequest } from "@paygentic/sdk/models/operations";

let value: CreateEntitlementGrantRequest = {
  entitlementId: "<id>",
  createGrantRequest: {
    amount: 7733.22,
    idempotencyKey: "<value>",
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `entitlementId`                                                 | *string*                                                        | :heavy_check_mark:                                              | The unique identifier of the entitlement to grant credits to.   |
| `createGrantRequest`                                            | [models.CreateGrantRequest](../../models/creategrantrequest.md) | :heavy_check_mark:                                              | N/A                                                             |