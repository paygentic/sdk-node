# PoolGrantPurchaseAccepted

## Example Usage

```typescript
import { PoolGrantPurchaseAccepted } from "@paygentic/sdk/models";

let value: PoolGrantPurchaseAccepted = {
  processing: false,
  invoiceId: "<id>",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `processing`                                                                       | *boolean*                                                                          | :heavy_check_mark:                                                                 | True while the invoice's settlement is still in progress.                          |
| `invoiceId`                                                                        | *string*                                                                           | :heavy_check_mark:                                                                 | The invoice ID the caller can poll or retry against with the same idempotency key. |