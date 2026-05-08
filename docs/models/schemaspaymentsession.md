# SchemasPaymentSession

## Example Usage

```typescript
import { SchemasPaymentSession } from "@paygentic/sdk/models";

let value: SchemasPaymentSession = {
  object: "payment_session",
  id: "<id>",
  entityType: "<value>",
  entityId: "<id>",
  amount: "489.73",
  currency: "Syrian Pound",
  status: "failed",
  createdAt: new Date("2026-08-10T05:41:33.173Z"),
  updatedAt: new Date("2026-05-22T05:48:04.758Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.SchemasPaymentSessionObject](../models/schemaspaymentsessionobject.md)                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Payment session ID (ps_*).                                                                    |
| `entityType`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Type of entity the session pays for (invoice, subscription, payment, topup).                  |
| `entityId`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ID of the entity the session pays for.                                                        |
| `amount`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Amount in decimal dollars.                                                                    |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ISO 4217 currency code.                                                                       |
| `status`                                                                                      | [models.SchemasPaymentSessionStatus](../models/schemaspaymentsessionstatus.md)                | :heavy_check_mark:                                                                            | Lifecycle status of the session.                                                              |
| `merchantPaymentAccountId`                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | Stripe Connect account ID (acct_*) when the session is routed to a connected account.         |
| `completedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Timestamp the session reached terminal completion. Null until the session completes.          |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |