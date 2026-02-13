# UpdateFeatureRequestBody

## Example Usage

```typescript
import { UpdateFeatureRequestBody } from "@paygentic/sdk/models/operations";

let value: UpdateFeatureRequestBody = {};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `key`                                                                              | *string*                                                                           | :heavy_minus_sign:                                                                 | Updated feature key slug. Sample values: 'increased-api-limit', 'new-storage-tier' |
| `name`                                                                             | *string*                                                                           | :heavy_minus_sign:                                                                 | Updated feature name.                                                              |
| `type`                                                                             | [operations.UpdateFeatureType](../../models/operations/updatefeaturetype.md)       | :heavy_minus_sign:                                                                 | Updated feature type                                                               |
| `metadata`                                                                         | Record<string, *string*>                                                           | :heavy_minus_sign:                                                                 | Updated metadata for the feature                                                   |