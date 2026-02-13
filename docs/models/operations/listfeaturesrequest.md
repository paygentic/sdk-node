# ListFeaturesRequest

## Example Usage

```typescript
import { ListFeaturesRequest } from "@paygentic/sdk/models/operations";

let value: ListFeaturesRequest = {
  productId: "<id>",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `productId`                                                                                              | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The product ID to filter features by                                                                     |
| `key`                                                                                                    | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Optional feature key to filter by. If provided, returns only the feature matching both productId and key |
| `limit`                                                                                                  | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Number of features to return.                                                                            |
| `offset`                                                                                                 | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Number of features to skip.                                                                              |