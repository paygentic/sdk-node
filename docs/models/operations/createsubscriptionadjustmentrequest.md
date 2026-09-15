# CreateSubscriptionAdjustmentRequest

## Example Usage

```typescript
import { CreateSubscriptionAdjustmentRequest } from "@paygentic/sdk/models/operations";

let value: CreateSubscriptionAdjustmentRequest = {
  id: "<id>",
  createSubscriptionAdjustmentRequest: {
    type: "percentageDiscount",
    percentageDiscount: "<value>",
    effectiveFrom: new Date("2025-01-05T00:51:25.114Z"),
  },
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `id`                                         | *string*                                     | :heavy_check_mark:                           | The subscription ID                          |
| `createSubscriptionAdjustmentRequest`        | *models.CreateSubscriptionAdjustmentRequest* | :heavy_check_mark:                           | N/A                                          |