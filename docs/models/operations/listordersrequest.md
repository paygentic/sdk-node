# ListOrdersRequest

## Example Usage

```typescript
import { ListOrdersRequest } from "@paygentic/sdk/models/operations";

let value: ListOrdersRequest = {};
```

## Fields

| Field                                                                      | Type                                                                       | Required                                                                   | Description                                                                |
| -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| `merchantId`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | Filter by merchant                                                         |
| `customerId`                                                               | *string*                                                                   | :heavy_minus_sign:                                                         | Filter by customer                                                         |
| `status`                                                                   | [operations.ListOrdersStatus](../../models/operations/listordersstatus.md) | :heavy_minus_sign:                                                         | Filter by status                                                           |
| `type`                                                                     | [operations.ListOrdersType](../../models/operations/listorderstype.md)     | :heavy_minus_sign:                                                         | Filter by type                                                             |
| `limit`                                                                    | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |
| `offset`                                                                   | *number*                                                                   | :heavy_minus_sign:                                                         | N/A                                                                        |