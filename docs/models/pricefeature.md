# PriceFeature

## Example Usage

```typescript
import { PriceFeature } from "@paygentic/sdk/models";

let value: PriceFeature = {
  id: "<id>",
  featureId: "<id>",
  entitlementTemplate: {},
};
```

## Fields

| Field                                                          | Type                                                           | Required                                                       | Description                                                    |
| -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `id`                                                           | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `featureId`                                                    | *string*                                                       | :heavy_check_mark:                                             | N/A                                                            |
| `entitlementTemplate`                                          | Record<string, *any*>                                          | :heavy_check_mark:                                             | N/A                                                            |
| `feature`                                                      | [models.PriceFeatureFeature](../models/pricefeaturefeature.md) | :heavy_minus_sign:                                             | N/A                                                            |