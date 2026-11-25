# CreateCreditPoolPurchaseRequest

## Example Usage

```typescript
import { CreateCreditPoolPurchaseRequest } from "@paygentic/sdk/models/operations";

let value: CreateCreditPoolPurchaseRequest = {
  id: "<id>",
  poolGrantPurchaseRequest: {
    grantAmount: 2853.17,
    idempotencyKey: "<value>",
  },
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `id`                                                                        | *string*                                                                    | :heavy_check_mark:                                                          | N/A                                                                         |
| `poolGrantPurchaseRequest`                                                  | [models.PoolGrantPurchaseRequest](../../models/poolgrantpurchaserequest.md) | :heavy_check_mark:                                                          | N/A                                                                         |