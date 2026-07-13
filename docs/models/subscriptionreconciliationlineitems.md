# SubscriptionReconciliationLineItems

## Example Usage

```typescript
import { SubscriptionReconciliationLineItems } from "@paygentic/sdk/models";

let value: SubscriptionReconciliationLineItems = {
  created: 196846,
  removed: 269156,
};
```

## Fields

| Field                                                                                                                                                  | Type                                                                                                                                                   | Required                                                                                                                                               | Description                                                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `created`                                                                                                                                              | *number*                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | Number of features newly billed on the subscription by this reconciliation. A dry-run preview returns the same count as the applied run.               |
| `removed`                                                                                                                                              | *number*                                                                                                                                               | :heavy_check_mark:                                                                                                                                     | Number of features whose billing was removed from the subscription's upcoming (not-yet-invoiced) invoice because their price is no longer on the plan. |
| `syncFailed`                                                                                                                                           | *boolean*                                                                                                                                              | :heavy_minus_sign:                                                                                                                                     | True when entitlements were provisioned successfully but the line-item synchronization step failed. Safe to retry.                                     |