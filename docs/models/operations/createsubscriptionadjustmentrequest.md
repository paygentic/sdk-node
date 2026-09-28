# CreateSubscriptionAdjustmentRequest

## Example Usage

```typescript
import { CreateSubscriptionAdjustmentRequest } from "@paygentic/sdk/models/operations";

let value: CreateSubscriptionAdjustmentRequest = {
  id: "<id>",
  createSubscriptionAdjustmentRequest: {
    type: "usageDiscount",
    usageDiscount: "<value>",
    targetPriceIds: [
      "<value 1>",
    ],
    effectiveFrom: new Date("2025-10-02T14:34:34.884Z"),
  },
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `id`                                         | *string*                                     | :heavy_check_mark:                           | The subscription ID                          |
| `createSubscriptionAdjustmentRequest`        | *models.CreateSubscriptionAdjustmentRequest* | :heavy_check_mark:                           | N/A                                          |