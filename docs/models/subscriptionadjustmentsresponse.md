# SubscriptionAdjustmentsResponse

## Example Usage

```typescript
import { SubscriptionAdjustmentsResponse } from "@paygentic/sdk/models";

let value: SubscriptionAdjustmentsResponse = {
  data: [
    {
      object: "subscriptionAdjustment",
      id: "<id>",
      subscriptionId: "<id>",
      type: "maximumQuantity",
      percentageDiscount: "<value>",
      usageDiscount: "<value>",
      minimumQuantity: "<value>",
      maximumQuantity: "<value>",
      targetPriceIds: [
        "<value 1>",
        "<value 2>",
        "<value 3>",
      ],
      effectiveFrom: new Date("2024-11-11T04:29:18.664Z"),
      effectiveTo: new Date("2024-03-18T22:34:26.648Z"),
      description:
        "hmph for yuck expense coast er neglected economise programme",
      createdAt: new Date("2024-04-17T06:14:00.713Z"),
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `data`                                                                 | [models.SubscriptionAdjustment](../models/subscriptionadjustment.md)[] | :heavy_check_mark:                                                     | N/A                                                                    |
| `pagination`                                                           | [models.OffsetPagination](../models/offsetpagination.md)               | :heavy_check_mark:                                                     | Offset-based pagination response.                                      |