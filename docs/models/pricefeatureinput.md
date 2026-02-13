# PriceFeatureInput

## Example Usage

```typescript
import { PriceFeatureInput } from "@paygentic/sdk/models";

let value: PriceFeatureInput = {
  featureId: "<id>",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `featureId`                                                      | *string*                                                         | :heavy_check_mark:                                               | The feature to associate with this price                         |
| `entitlementTemplate`                                            | Record<string, *any*>                                            | :heavy_minus_sign:                                               | Template for entitlement values when this feature is provisioned |