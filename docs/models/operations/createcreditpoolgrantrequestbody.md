# CreateCreditPoolGrantRequestBody

## Example Usage

```typescript
import { CreateCreditPoolGrantRequestBody } from "@paygentic/sdk/models/operations";

let value: CreateCreditPoolGrantRequestBody = {
  amount: 21.2,
};
```

## Fields

| Field                                                                                                     | Type                                                                                                      | Required                                                                                                  | Description                                                                                               |
| --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| `amount`                                                                                                  | *number*                                                                                                  | :heavy_check_mark:                                                                                        | Credits to allocate (in the pool's pricing unit).                                                         |
| `priority`                                                                                                | *number*                                                                                                  | :heavy_minus_sign:                                                                                        | Drawdown priority (lower = consumed first). Defaults to 0.                                                |
| `effectiveAt`                                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)             | :heavy_minus_sign:                                                                                        | When the block becomes active. Defaults to now (or the customer's active-subscription test-clock time).   |
| `recurrencePeriod`                                                                                        | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | ISO-8601 duration (e.g. `P1M`). When set, `amount` is re-added each interval within the block's envelope. |
| `recurrenceAnchor`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)             | :heavy_minus_sign:                                                                                        | Recurrence phase anchor. Defaults to `effectiveAt`. Only valid with `recurrencePeriod`.                   |
| `expiresAt`                                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)             | :heavy_minus_sign:                                                                                        | When the block expires (per-block expiry).                                                                |
| `idempotencyKey`                                                                                          | *string*                                                                                                  | :heavy_minus_sign:                                                                                        | Idempotency key; a repeat with the same key returns the existing grant.                                   |