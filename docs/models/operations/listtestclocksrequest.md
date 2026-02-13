# ListTestClocksRequest

## Example Usage

```typescript
import { ListTestClocksRequest } from "@paygentic/sdk/models/operations";

let value: ListTestClocksRequest = {};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `limit`                                                                                                  | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Number of items to return                                                                                |
| `merchantId`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Filter test clocks by merchant ID. If not provided, will be extracted from authenticated user's context. |
| `offset`                                                                                                 | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Number of items to skip                                                                                  |