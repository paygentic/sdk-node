# Features

## Example Usage

```typescript
import { Features } from "@paygentic/sdk/models";

let value: Features = {
  added: [],
  skipped: [],
  removed: [],
  failed: [
    {
      featureId: "<id>",
      featureKey: "<value>",
      reason: "entitlement_failed",
    },
  ],
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `added`                                                                                                                                   | [models.ReconciledFeatureAdded](../models/reconciledfeatureadded.md)[]                                                                    | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |
| `skipped`                                                                                                                                 | [models.ReconciledFeatureSkipped](../models/reconciledfeatureskipped.md)[]                                                                | :heavy_check_mark:                                                                                                                        | Features the subscription already had an active entitlement for — left unchanged.                                                         |
| `removed`                                                                                                                                 | [models.ReconciledFeatureRemoved](../models/reconciledfeatureremoved.md)[]                                                                | :heavy_check_mark:                                                                                                                        | Features no longer on the plan: their entitlement was canceled and grants voided so the subscription matches the plan's current features. |
| `failed`                                                                                                                                  | [models.ReconciledFeatureFailed](../models/reconciledfeaturefailed.md)[]                                                                  | :heavy_check_mark:                                                                                                                        | Features that could not be fully provisioned. Never billed by this call.                                                                  |