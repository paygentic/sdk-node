# CreditPoolLedgerEntryGrant

The grant this entry relates to — the grant that funded the pool for `increment`, or the grant whose balance changed for `decrement`, `void`, and `expiration`.

## Example Usage

```typescript
import { CreditPoolLedgerEntryGrant } from "@paygentic/sdk/models";

let value: CreditPoolLedgerEntryGrant = {
  id: "<id>",
  expiresAt: new Date("2025-07-11T23:58:05.204Z"),
  conversionRate: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | The grant's own expiry, or null if it never expires.                                          |
| `conversionRate`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | The pool's pricing-unit conversion rate ($ per credit), as a decimal string.                  |