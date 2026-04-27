# Entitlement

## Example Usage

```typescript
import { Entitlement } from "@paygentic/sdk/models";

let value: Entitlement = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  status: "expired",
  activeFrom: new Date("2026-09-03T17:39:40.646Z"),
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
| `object`                                                                                      | [models.EntitlementObject](../models/entitlementobject.md)                                    | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the entitlement.                                                        |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a customer                                                              |
| `featureId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The feature this entitlement grants access to.                                                |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | The subscription this entitlement is associated with, if any.                                 |
| `status`                                                                                      | [models.EntitlementStatus](../models/entitlementstatus.md)                                    | :heavy_check_mark:                                                                            | Current status of the entitlement.                                                            |
| `activeFrom`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the entitlement becomes active.                                                          |
| `activeTo`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the entitlement expires. Null means no expiration.                                       |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | Configuration values for static features.                                                     |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_minus_sign:                                                                            | Additional metadata for the entitlement.                                                      |