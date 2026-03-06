# ListPaymentSessionsRequest

## Example Usage

```typescript
import { ListPaymentSessionsRequest } from "@paygentic/sdk/models/operations";

let value: ListPaymentSessionsRequest = {};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `merchantId`                                                                                      | *string*                                                                                          | :heavy_minus_sign:                                                                                | Merchant organization ID. Required when using an API key that is not scoped to a single merchant. |
| `status`                                                                                          | [operations.ListPaymentSessionsStatus](../../models/operations/listpaymentsessionsstatus.md)      | :heavy_minus_sign:                                                                                | Filter by payment status.                                                                         |
| `customerId`                                                                                      | *string*                                                                                          | :heavy_minus_sign:                                                                                | Filter by customer ID.                                                                            |
| `limit`                                                                                           | *number*                                                                                          | :heavy_minus_sign:                                                                                | Number of payments to return.                                                                     |
| `offset`                                                                                          | *number*                                                                                          | :heavy_minus_sign:                                                                                | Number of payments to skip.                                                                       |