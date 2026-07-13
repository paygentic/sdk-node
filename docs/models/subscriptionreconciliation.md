# SubscriptionReconciliation

## Example Usage

```typescript
import { SubscriptionReconciliation } from "@paygentic/sdk/models";

let value: SubscriptionReconciliation = {
  object: "subscriptionReconciliation",
  dryRun: false,
  features: {
    added: [
      {
        featureId: "<id>",
        featureKey: "<value>",
        billed: true,
      },
    ],
    skipped: [],
    removed: [
      {
        featureId: "<id>",
        featureKey: "<value>",
      },
    ],
    failed: [
      {
        featureId: "<id>",
        featureKey: "<value>",
        reason: "entitlement_failed",
      },
    ],
  },
  lineItems: {
    created: 925542,
    removed: 235568,
  },
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `object`                                                                                       | [models.SubscriptionReconciliationObject](../models/subscriptionreconciliationobject.md)       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `dryRun`                                                                                       | *boolean*                                                                                      | :heavy_check_mark:                                                                             | True when this reconciliation was a preview — no entitlement, grant, or line item was created. |
| `features`                                                                                     | [models.Features](../models/features.md)                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `lineItems`                                                                                    | [models.SubscriptionReconciliationLineItems](../models/subscriptionreconciliationlineitems.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |