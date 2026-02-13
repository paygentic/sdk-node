# ListFeesRequest

## Example Usage

```typescript
import { ListFeesRequest } from "@paygentic/sdk/models/operations";

let value: ListFeesRequest = {
  merchantId: "<id>",
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `limit`                                  | *number*                                 | :heavy_minus_sign:                       | Number of fees to return.                |
| `merchantId`                             | *string*                                 | :heavy_check_mark:                       | Filter fees by merchant organization ID. |
| `offset`                                 | *number*                                 | :heavy_minus_sign:                       | Number of fees to skip.                  |
| `productId`                              | *string*                                 | :heavy_minus_sign:                       | Filter fees by product ID.               |