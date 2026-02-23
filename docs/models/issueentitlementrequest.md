# IssueEntitlementRequest

## Example Usage

```typescript
import { IssueEntitlementRequest } from "@paygentic/sdk/models";

let value: IssueEntitlementRequest = {
  customerId: "<id>",
  featureId: "<id>",
  template: {
    type: "metered",
    usagePeriod: {
      interval: "<value>",
    },
  },
};
```

## Fields

| Field                                                                                                                                       | Type                                                                                                                                        | Required                                                                                                                                    | Description                                                                                                                                 |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| `customerId`                                                                                                                                | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | Unique identifier for a customer                                                                                                            |
| `featureId`                                                                                                                                 | *string*                                                                                                                                    | :heavy_check_mark:                                                                                                                          | The feature to grant access to.                                                                                                             |
| `template`                                                                                                                                  | *models.EntitlementTemplate*                                                                                                                | :heavy_check_mark:                                                                                                                          | Template for the entitlement. Boolean for simple on/off features, static for features with configuration, metered for usage-based features. |
| `activeFrom`                                                                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                               | :heavy_minus_sign:                                                                                                                          | When the entitlement becomes active. Defaults to now.                                                                                       |
| `activeTo`                                                                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                               | :heavy_minus_sign:                                                                                                                          | When the entitlement expires. Null means no expiration.                                                                                     |
| `subscriptionId`                                                                                                                            | *string*                                                                                                                                    | :heavy_minus_sign:                                                                                                                          | Optional subscription ID to associate with this entitlement.                                                                                |
| `metadata`                                                                                                                                  | Record<string, *string*>                                                                                                                    | :heavy_minus_sign:                                                                                                                          | Additional metadata for the entitlement.                                                                                                    |