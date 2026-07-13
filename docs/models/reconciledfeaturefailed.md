# ReconciledFeatureFailed

## Example Usage

```typescript
import { ReconciledFeatureFailed } from "@paygentic/sdk/models";

let value: ReconciledFeatureFailed = {
  featureId: "<id>",
  featureKey: "<value>",
  reason: "entitlement_failed",
};
```

## Fields

| Field                                                                                                                                                                           | Type                                                                                                                                                                            | Required                                                                                                                                                                        | Description                                                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `featureId`                                                                                                                                                                     | *string*                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                              | N/A                                                                                                                                                                             |
| `featureKey`                                                                                                                                                                    | *string*                                                                                                                                                                        | :heavy_check_mark:                                                                                                                                                              | N/A                                                                                                                                                                             |
| `reason`                                                                                                                                                                        | [models.Reason](../models/reason.md)                                                                                                                                            | :heavy_check_mark:                                                                                                                                                              | Coded failure reason. `grant_mint_failed` means the entitlement was created but its initial metered grant could not be minted; re-running this reconciliation retries the mint. |