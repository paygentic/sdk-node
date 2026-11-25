# ListCreditPoolsRequest

## Example Usage

```typescript
import { ListCreditPoolsRequest } from "@paygentic/sdk/models/operations";

let value: ListCreditPoolsRequest = {};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `merchantId`                                                                           | *string*                                                                               | :heavy_minus_sign:                                                                     | Filter credit pools by merchant organization id (resolved through the pool's customer) |
| `customerId`                                                                           | *string*                                                                               | :heavy_minus_sign:                                                                     | Filter credit pools by customer id                                                     |
| `pricingUnitId`                                                                        | *string*                                                                               | :heavy_minus_sign:                                                                     | Filter credit pools by pricing unit id                                                 |
| `limit`                                                                                | *number*                                                                               | :heavy_minus_sign:                                                                     | Maximum credit pools to return                                                         |
| `offset`                                                                               | *number*                                                                               | :heavy_minus_sign:                                                                     | Zero-based offset for pagination                                                       |