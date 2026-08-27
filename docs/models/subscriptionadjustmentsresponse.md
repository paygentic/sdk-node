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
      type: "percentageDiscount",
      percentageDiscount: "<value>",
      effectiveFrom: new Date("2026-05-22T17:26:28.653Z"),
      effectiveTo: new Date("2026-12-01T10:13:41.565Z"),
      description:
        "ew language unexpectedly fatally carelessly even sanity insidious",
      createdAt: new Date("2025-08-27T09:09:53.038Z"),
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