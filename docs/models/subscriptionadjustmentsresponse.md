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
      type: "usageDiscount",
      percentageDiscount: "<value>",
      usageDiscount: "<value>",
      targetPriceIds: [
        "<value 1>",
        "<value 2>",
      ],
      effectiveFrom: new Date("2026-02-12T06:29:40.059Z"),
      effectiveTo: new Date("2024-11-11T04:29:18.664Z"),
      description: "incidentally officially why",
      createdAt: new Date("2024-04-12T05:47:40.543Z"),
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