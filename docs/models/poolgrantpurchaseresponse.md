# PoolGrantPurchaseResponse

## Example Usage

```typescript
import { PoolGrantPurchaseResponse } from "@paygentic/sdk/models";

let value: PoolGrantPurchaseResponse = {
  invoiceId: "<id>",
  poolId: "<id>",
  grantAmount: 6885.8,
  price: "390.75",
  currency: "Aruban Guilder",
  paymentSessions: [
    {
      url: "https://untidy-dish.name/",
    },
  ],
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                 | [models.PoolGrantPurchaseResponseObject](../models/poolgrantpurchaseresponseobject.md)                   | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |
| `invoiceId`                                                                                              | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The invoice ID for this grant purchase.                                                                  |
| `poolId`                                                                                                 | *string*                                                                                                 | :heavy_check_mark:                                                                                       | N/A                                                                                                      |
| `grantAmount`                                                                                            | *number*                                                                                                 | :heavy_check_mark:                                                                                       | The number of credits that will be granted on payment.                                                   |
| `price`                                                                                                  | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The price in decimal format (e.g., '5.00').                                                              |
| `currency`                                                                                               | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The three-letter ISO 4217 currency code (e.g., 'usd').                                                   |
| `paymentSessions`                                                                                        | [models.PoolGrantPurchaseResponsePaymentSession](../models/poolgrantpurchaseresponsepaymentsession.md)[] | :heavy_check_mark:                                                                                       | Payment session(s) for the customer to complete the purchase.                                            |