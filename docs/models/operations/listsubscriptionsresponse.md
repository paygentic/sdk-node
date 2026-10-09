# ListSubscriptionsResponse

List of subscriptions

## Example Usage

```typescript
import { ListSubscriptionsResponse } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionsResponse = {
  data: [
    {
      id: "<id>",
      object: "subscription",
      merchantId: "<id>",
      createdAt: new Date("2026-12-18T22:44:51.894Z"),
      customerId: "<id>",
      name: "<value>",
      planId: "<id>",
      versionPolicy: "pinned",
      startedAt: new Date("2026-04-07T23:34:54.083Z"),
      elapsedPeriodBilling: "per_period",
      billingStartsAt: new Date("2026-08-24T10:47:22.288Z"),
      billingAnchor: new Date("2026-10-25T13:27:20.061Z"),
      billingCadence: "P1M",
      status: "terminated",
      updatedAt: new Date("2026-11-02T05:52:26.817Z"),
      paymentTermDays: 181887,
    },
  ],
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.Subscription](../../models/subscription.md)[]       | :heavy_minus_sign:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_minus_sign:                                          | Offset-based pagination response.                           |