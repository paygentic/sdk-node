# MeteredEntitlementDetail

Common fields shared by all entitlement types.

## Example Usage

```typescript
import { MeteredEntitlementDetail } from "@paygentic/sdk/models";

let value: MeteredEntitlementDetail = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "metered",
  status: "active",
  activeFrom: new Date("2025-08-02T04:33:12.548Z"),
  hasAccess: true,
  balance: 8439.55,
  usageInPeriod: 8984.39,
  overage: 9117.79,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.MeteredEntitlementDetailObject](../models/meteredentitlementdetailobject.md)          | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the entitlement.                                                        |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a customer                                                              |
| `featureId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The feature this entitlement grants access to.                                                |
| `featureKey`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The unique key identifying the feature.                                                       |
| `featureType`                                                                                 | *"metered"*                                                                                   | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | The subscription this entitlement is associated with, if any.                                 |
| `status`                                                                                      | [models.MeteredEntitlementDetailStatus](../models/meteredentitlementdetailstatus.md)          | :heavy_check_mark:                                                                            | Current status of the entitlement.                                                            |
| `activeFrom`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement becomes active.                                                          |
| `activeTo`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the entitlement expires. Null means no expiration.                                       |
| `hasAccess`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether the customer currently has active access to this entitlement.                         |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | Additional metadata for the entitlement.                                                      |
| `balance`                                                                                     | *number*                                                                                      | :heavy_check_mark:                                                                            | Remaining grant balance for the current period.                                               |
| `usageInPeriod`                                                                               | *number*                                                                                      | :heavy_check_mark:                                                                            | Total usage consumed in the current billing period.                                           |
| `overage`                                                                                     | *number*                                                                                      | :heavy_check_mark:                                                                            | Amount of usage exceeding the granted balance.                                                |
| `currentPeriodStart`                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Start of the current usage period.                                                            |
| `currentPeriodEnd`                                                                            | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | End of the current usage period.                                                              |