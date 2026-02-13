# ListProductsResponse

List of products

## Example Usage

```typescript
import { ListProductsResponse } from "@paygentic/sdk/models/operations";

let value: ListProductsResponse = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.Product](../../models/product.md)[]                 | :heavy_minus_sign:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_minus_sign:                                          | Offset-based pagination response.                           |