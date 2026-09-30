# SubscriptionIntervalsResponse

## Example Usage

```typescript
import { SubscriptionIntervalsResponse } from "@paygentic/sdk/models";

let value: SubscriptionIntervalsResponse = {
  intervals: [
    {
      id: "<id>",
      priceId: "<id>",
      priceKey: "<value>",
      kind: "plan_line",
      planVersionId: "<id>",
      unitPrice: "<value>",
      baseQuantity: "<value>",
      quantityTransitions: [],
      billingCadence: "<value>",
      billingMode: "arrears",
      billDate: new Date("2026-06-07T06:45:11.123Z"),
      startDate: new Date("2025-06-01T20:55:20.444Z"),
      endDate: new Date("2026-01-17T19:57:45.203Z"),
    },
  ],
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `intervals`                                                                        | [models.SubscriptionInterval](../models/subscriptioninterval.md)[]                 | :heavy_check_mark:                                                                 | The subscription's price intervals, ordered by start date. Empty when it has none. |