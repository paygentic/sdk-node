# ListPlansRequest

## Example Usage

```typescript
import { ListPlansRequest } from "@paygentic/sdk/models/operations";

let value: ListPlansRequest = {};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `limit`                                  | *number*                                 | :heavy_minus_sign:                       | Number of plans to return                |
| `merchantId`                             | *string*                                 | :heavy_minus_sign:                       | Filter plans by merchant organization ID |
| `offset`                                 | *number*                                 | :heavy_minus_sign:                       | Number of plans to skip                  |
| `productId`                              | *string*                                 | :heavy_minus_sign:                       | Filter plans by product ID               |