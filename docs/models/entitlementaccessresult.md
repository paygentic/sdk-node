# EntitlementAccessResult

A customer's entitlement to a specific feature.

## Example Usage

```typescript
import { EntitlementAccessResult } from "@paygentic/sdk/models";

let value: EntitlementAccessResult = {
  hasAccess: true,
  featureKey: "<value>",
  featureType: "static",
  entitlementId: "<id>",
  productId: "<id>",
  activeFrom: new Date("2025-02-08T05:50:08.708Z"),
  status: "active",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `hasAccess`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether the customer currently has active access to this feature.                             |
| `featureKey`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The unique key identifying the feature.                                                       |
| `featureType`                                                                                 | [models.EntitlementAccessResultFeatureType](../models/entitlementaccessresultfeaturetype.md)  | :heavy_check_mark:                                                                            | The type of feature: `boolean` (on/off), `static` (with config), or `metered` (usage-based).  |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_minus_sign:                                                                            | Configuration values for `static` features. Null for other types.                             |
| `entitlementId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for this entitlement.                                                       |
| `productId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a product                                                               |
| `activeFrom`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement becomes active.                                                          |
| `activeTo`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the entitlement expires. Null means no expiration.                                       |
| `status`                                                                                      | [models.EntitlementAccessResultStatus](../models/entitlementaccessresultstatus.md)            | :heavy_check_mark:                                                                            | Current status of the entitlement.                                                            |