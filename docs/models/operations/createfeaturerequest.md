# CreateFeatureRequest

## Example Usage

```typescript
import { CreateFeatureRequest } from "@paygentic/sdk/models/operations";

let value: CreateFeatureRequest = {
  key: "<key>",
  name: "<value>",
  merchantId: "<id>",
  productId: "<id>",
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `key`                                                                                                            | *string*                                                                                                         | :heavy_check_mark:                                                                                               | Unique slug identifier for the feature within the product. Must be lowercase letters, numbers, and hyphens only. |
| `name`                                                                                                           | *string*                                                                                                         | :heavy_check_mark:                                                                                               | Human-readable feature name shown to customers.                                                                  |
| `type`                                                                                                           | [operations.CreateFeatureType](../../models/operations/createfeaturetype.md)                                     | :heavy_minus_sign:                                                                                               | Feature type: 'metered' for usage-based features, 'static' for fixed allocations, 'boolean' for on/off features  |
| `merchantId`                                                                                                     | *string*                                                                                                         | :heavy_check_mark:                                                                                               | Unique identifier for an organization                                                                            |
| `productId`                                                                                                      | *string*                                                                                                         | :heavy_check_mark:                                                                                               | Unique identifier for a product                                                                                  |
| `metadata`                                                                                                       | Record<string, *string*>                                                                                         | :heavy_minus_sign:                                                                                               | Optional key-value metadata storage for feature information.                                                     |