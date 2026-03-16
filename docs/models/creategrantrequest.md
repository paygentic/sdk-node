# CreateGrantRequest

## Example Usage

```typescript
import { CreateGrantRequest } from "@paygentic/sdk/models";

let value: CreateGrantRequest = {
  amount: 6518.9,
  idempotencyKey: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `amount`                                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | The number of credits to grant.                                                               |
| `effectiveAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the grant becomes effective. Defaults to now.                                            |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the grant expires. If omitted, the grant does not expire.                                |
| `idempotencyKey`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Idempotency key to prevent duplicate grants. Must be unique per entitlement.                  |