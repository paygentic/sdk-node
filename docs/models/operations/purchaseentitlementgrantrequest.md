# PurchaseEntitlementGrantRequest

## Example Usage

```typescript
import { PurchaseEntitlementGrantRequest } from "@paygentic/sdk/models/operations";

let value: PurchaseEntitlementGrantRequest = {
  entitlementId: "<id>",
  purchaseGrantRequest: {
    amount: 4550.36,
    price: "576.18",
    idempotencyKey: "<value>",
  },
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `entitlementId`                                                     | *string*                                                            | :heavy_check_mark:                                                  | The unique identifier of the entitlement to purchase credits for.   |
| `purchaseGrantRequest`                                              | [models.PurchaseGrantRequest](../../models/purchasegrantrequest.md) | :heavy_check_mark:                                                  | N/A                                                                 |