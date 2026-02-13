# ListSubscriptionsRequest

## Example Usage

```typescript
import { ListSubscriptionsRequest } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionsRequest = {};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `consumerId`                                                                             | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |
| `customerId`                                                                             | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |
| `limit`                                                                                  | *string*                                                                                 | :heavy_minus_sign:                                                                       | Number of subscriptions to return                                                        |
| `merchantId`                                                                             | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |
| `offset`                                                                                 | *string*                                                                                 | :heavy_minus_sign:                                                                       | Number of subscriptions to skip                                                          |
| `status`                                                                                 | [operations.ListSubscriptionsStatus](../../models/operations/listsubscriptionsstatus.md) | :heavy_minus_sign:                                                                       | N/A                                                                                      |