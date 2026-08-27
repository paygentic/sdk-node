# CreateSubscriptionAdjustmentRequest

## Example Usage

```typescript
import { CreateSubscriptionAdjustmentRequest } from "@paygentic/sdk/models/operations";

let value: CreateSubscriptionAdjustmentRequest = {
  id: "<id>",
  createSubscriptionAdjustmentRequest: {
    type: "percentageDiscount",
    percentageDiscount: "<value>",
    effectiveFrom: new Date("2025-12-21T02:17:09.871Z"),
    idempotencyKey: "adj_fy26_growth_001",
  },
};
```

## Fields

| Field                                                                                             | Type                                                                                              | Required                                                                                          | Description                                                                                       |
| ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `id`                                                                                              | *string*                                                                                          | :heavy_check_mark:                                                                                | The subscription ID                                                                               |
| `createSubscriptionAdjustmentRequest`                                                             | [models.CreateSubscriptionAdjustmentRequest](../../models/createsubscriptionadjustmentrequest.md) | :heavy_check_mark:                                                                                | N/A                                                                                               |