# TerminateSubscriptionRequestBody

## Example Usage

```typescript
import { TerminateSubscriptionRequestBody } from "@paygentic/sdk/models/operations";

let value: TerminateSubscriptionRequestBody = {
  reason: "<value>",
};
```

## Fields

| Field                                                                                                                                                                                            | Type                                                                                                                                                                                             | Required                                                                                                                                                                                         | Description                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `reason`                                                                                                                                                                                         | *string*                                                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                               | Cancellation explanation text. Sample values: 'Customer requested cancellation', 'Payment failure', 'Service migration', 'Contract expiration'                                                   |
| `changeReason`                                                                                                                                                                                   | [models.ChangeReason](../../models/changereason.md)                                                                                                                                              | :heavy_minus_sign:                                                                                                                                                                               | Why a change was made. `correction` fixes data to match what was agreed; `migration` moves a contract from another system; `commercial` is a real change to the deal. Defaults to `unspecified`. |