# ListCostsRequest

## Example Usage

```typescript
import { ListCostsRequest } from "@paygentic/sdk/models/operations";

let value: ListCostsRequest = {};
```

## Fields

| Field                                                                                                                     | Type                                                                                                                      | Required                                                                                                                  | Description                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `merchantId`                                                                                                              | *string*                                                                                                                  | :heavy_minus_sign:                                                                                                        | Filter costs by merchant organization ID. If omitted, defaults to the merchant associated with the authenticated API key. |
| `productId`                                                                                                               | *string*                                                                                                                  | :heavy_minus_sign:                                                                                                        | Filter costs by product ID.                                                                                               |
| `limit`                                                                                                                   | *number*                                                                                                                  | :heavy_minus_sign:                                                                                                        | Number of costs to return.                                                                                                |
| `offset`                                                                                                                  | *number*                                                                                                                  | :heavy_minus_sign:                                                                                                        | Number of costs to skip.                                                                                                  |