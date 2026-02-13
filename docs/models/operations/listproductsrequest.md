# ListProductsRequest

## Example Usage

```typescript
import { ListProductsRequest } from "@paygentic/sdk/models/operations";

let value: ListProductsRequest = {};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `limit`                                     | *number*                                    | :heavy_minus_sign:                          | Number of products to return                |
| `merchantId`                                | *string*                                    | :heavy_minus_sign:                          | Filter products by merchant organization ID |
| `offset`                                    | *number*                                    | :heavy_minus_sign:                          | Number of products to skip                  |