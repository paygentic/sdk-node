# Grant

## Example Usage

```typescript
import { Grant } from "@paygentic/sdk/models";

let value: Grant = {
  id: "<id>",
  entitlementId: "<id>",
  amount: 8197.36,
  effectiveAt: new Date("2024-01-24T01:01:50.778Z"),
  createdAt: new Date("2025-04-24T07:46:14.368Z"),
  recurrencePeriod: null,
  idempotencyKey: null,
};
```

## Fields

| Field                                                                                               | Type                                                                                                | Required                                                                                            | Description                                                                                         |
| --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| `object`                                                                                            | [models.GrantObject](../models/grantobject.md)                                                      | :heavy_minus_sign:                                                                                  | N/A                                                                                                 |
| `id`                                                                                                | *string*                                                                                            | :heavy_check_mark:                                                                                  | Unique identifier for the grant.                                                                    |
| `entitlementId`                                                                                     | *string*                                                                                            | :heavy_check_mark:                                                                                  | The entitlement this grant belongs to.                                                              |
| `amount`                                                                                            | *number*                                                                                            | :heavy_check_mark:                                                                                  | The number of credits granted.                                                                      |
| `effectiveAt`                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)       | :heavy_check_mark:                                                                                  | When the grant becomes effective.                                                                   |
| `expiresAt`                                                                                         | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)       | :heavy_minus_sign:                                                                                  | When the grant expires. Null means no expiration.                                                   |
| `voidedAt`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)       | :heavy_minus_sign:                                                                                  | When the grant was voided. Null means the grant is active.                                          |
| `createdAt`                                                                                         | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)       | :heavy_check_mark:                                                                                  | When the grant was created.                                                                         |
| `recurrencePeriod`                                                                                  | *string*                                                                                            | :heavy_check_mark:                                                                                  | The recurrence interval (ISO 8601 duration) if this is a recurring grant. Null for one-time grants. |
| `idempotencyKey`                                                                                    | *string*                                                                                            | :heavy_check_mark:                                                                                  | The idempotency key used when creating this grant. Null if not provided.                            |