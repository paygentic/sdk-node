# ListAvailablePlansRequest

## Example Usage

```typescript
import { ListAvailablePlansRequest } from "@paygentic/sdk/models/operations";

let value: ListAvailablePlansRequest = {
  customerId: "<id>",
};
```

## Fields

| Field                                                                                      | Type                                                                                       | Required                                                                                   | Description                                                                                |
| ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------ |
| `customerId`                                                                               | *string*                                                                                   | :heavy_check_mark:                                                                         | The customer to check subscriptions for. The merchant is derived from the customer record. |
| `productId`                                                                                | *string*                                                                                   | :heavy_minus_sign:                                                                         | Optional filter by product ID                                                              |
| `search`                                                                                   | *string*                                                                                   | :heavy_minus_sign:                                                                         | Optional search text to filter plan names (case-insensitive)                               |
| `limit`                                                                                    | *number*                                                                                   | :heavy_minus_sign:                                                                         | Number of plans to return                                                                  |
| `offset`                                                                                   | *number*                                                                                   | :heavy_minus_sign:                                                                         | Number of plans to skip                                                                    |