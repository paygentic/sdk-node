# PurchaseGrantResponse

## Example Usage

```typescript
import { PurchaseGrantResponse } from "@paygentic/sdk/models";

let value: PurchaseGrantResponse = {
  invoiceId: "<id>",
  entitlementId: "<id>",
  grantAmount: 729630,
  price: "495.05",
  currency: "Guinea Franc",
  paymentSessions: [
    {
      url: "https://growing-silk.biz/",
    },
  ],
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [models.PurchaseGrantResponseObject](../models/purchasegrantresponseobject.md) | :heavy_minus_sign:                                                             | N/A                                                                            |
| `invoiceId`                                                                    | *string*                                                                       | :heavy_check_mark:                                                             | The invoice ID for this grant purchase.                                        |
| `entitlementId`                                                                | *string*                                                                       | :heavy_check_mark:                                                             | The entitlement that will receive the grant.                                   |
| `grantAmount`                                                                  | *number*                                                                       | :heavy_check_mark:                                                             | The number of credits that will be granted on payment.                         |
| `price`                                                                        | *string*                                                                       | :heavy_check_mark:                                                             | The price in decimal format (e.g., '5.00').                                    |
| `currency`                                                                     | *string*                                                                       | :heavy_check_mark:                                                             | The three-letter ISO 4217 currency code (e.g., 'usd').                         |
| `paymentSessions`                                                              | [models.PaymentSession](../models/paymentsession.md)[]                         | :heavy_check_mark:                                                             | Payment session(s) for the customer to complete the purchase.                  |