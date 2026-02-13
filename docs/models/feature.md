# Feature

## Example Usage

```typescript
import { Feature } from "@paygentic/sdk/models";

let value: Feature = {
  id: "<id>",
  key: "<key>",
  name: "<value>",
  type: "metered",
  merchantId: "<id>",
  productId: "<id>",
  metadata: {
    "key": "<value>",
  },
  createdAt: new Date("2025-04-19T20:45:48.067Z"),
  updatedAt: new Date("2024-06-02T20:10:17.196Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a feature                                                               |
| `object`                                                                                      | [models.FeatureObject](../models/featureobject.md)                                            | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `key`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.FeatureType](../models/featuretype.md)                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `productId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a product                                                               |
| `metadata`                                                                                    | Record<string, *string*>                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Timestamp when the feature was created                                                        |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Timestamp when the feature was last updated                                                   |