# StaticEntitlementDetail

Common fields shared by all entitlement types.

## Example Usage

```typescript
import { StaticEntitlementDetail } from "@paygentic/sdk/models";

let value: StaticEntitlementDetail = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "static",
  status: "canceled",
  activeFrom: new Date("2026-07-13T14:18:34.649Z"),
  hasAccess: true,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.StaticEntitlementDetailObject](../models/staticentitlementdetailobject.md)            | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the entitlement.                                                        |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a customer                                                              |
| `featureId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The feature this entitlement grants access to.                                                |
| `featureKey`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The unique key identifying the feature.                                                       |
| `featureType`                                                                                 | *"static"*                                                                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | The subscription this entitlement is associated with, if any.                                 |
| `status`                                                                                      | [models.StaticEntitlementDetailStatus](../models/staticentitlementdetailstatus.md)            | :heavy_check_mark:                                                                            | Current status of the entitlement.                                                            |
| `activeFrom`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement becomes active.                                                          |
| `activeTo`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the entitlement expires. Null means no expiration.                                       |
| `hasAccess`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether the customer currently has active access to this entitlement.                         |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | Additional metadata for the entitlement.                                                      |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_minus_sign:                                                                            | Configuration values for this entitlement.                                                    |