# StaticEntitlementListItem

Common fields shared by all entitlement list items. List items use `entitlementId` (not `id`) to preserve the original public field name on `/v1/entitlements`. The get-by-id endpoint returns the same object with a top-level `id` and `object: "entitlement"` instead.

## Example Usage

```typescript
import { StaticEntitlementListItem } from "@paygentic/sdk/models";

let value: StaticEntitlementListItem = {
  entitlementId: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "static",
  productId: "<id>",
  subscriptionId: null,
  status: "active",
  activeFrom: new Date("2026-03-27T08:08:50.344Z"),
  activeTo: new Date("2024-06-14T21:02:55.215Z"),
  hasAccess: true,
  metadata: {
    "key": "<value>",
    "key1": "<value>",
  },
  config: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `entitlementId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the entitlement.                                                        |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a customer                                                              |
| `featureId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The feature this entitlement grants access to.                                                |
| `featureKey`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The unique key identifying the feature.                                                       |
| `featureType`                                                                                 | *"static"*                                                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `productId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a product                                                               |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | The subscription this entitlement is associated with, if any.                                 |
| `status`                                                                                      | [models.EntitlementStatus](../models/entitlementstatus.md)                                    | :heavy_check_mark:                                                                            | Current status of the entitlement.                                                            |
| `activeFrom`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement becomes active.                                                          |
| `activeTo`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement expires. Null means no expiration.                                       |
| `hasAccess`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether the customer currently has active access to this entitlement.                         |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_check_mark:                                                                            | Additional metadata for the entitlement.                                                      |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | Configuration values for this entitlement.                                                    |