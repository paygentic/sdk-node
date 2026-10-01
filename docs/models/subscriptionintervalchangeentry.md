# SubscriptionIntervalChangeEntry

One interval that the change added, edited or removed, with its state before and after.

## Example Usage

```typescript
import { SubscriptionIntervalChangeEntry } from "@paygentic/sdk/models";

let value: SubscriptionIntervalChangeEntry = {
  intervalId: "<id>",
  before: {
    priceId: "<id>",
    priceKey: "<value>",
    planVersionId: "<id>",
    unitPrice: "<value>",
    resolvedUnitPrice: "<value>",
    baseQuantity: "<value>",
    quantityTransitions: [],
    billingCadence: "<value>",
    billingMode: "advance",
    billDate: new Date("2025-07-31T00:42:27.127Z"),
    startDate: new Date("2025-02-14T23:14:28.049Z"),
    endDate: new Date("2026-08-07T18:01:27.091Z"),
  },
  after: {
    priceId: "<id>",
    priceKey: "<value>",
    planVersionId: "<id>",
    unitPrice: "<value>",
    resolvedUnitPrice: "<value>",
    baseQuantity: "<value>",
    quantityTransitions: [],
    billingCadence: "<value>",
    billingMode: "arrears",
    billDate: new Date("2024-05-11T22:54:15.908Z"),
    startDate: new Date("2025-12-26T19:45:27.247Z"),
    endDate: new Date("2026-11-18T20:08:54.258Z"),
  },
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `intervalId`                                                                         | *string*                                                                             | :heavy_check_mark:                                                                   | N/A                                                                                  |
| `before`                                                                             | [models.SubscriptionIntervalChangeCopy](../models/subscriptionintervalchangecopy.md) | :heavy_check_mark:                                                                   | The interval before the edit. Null when the edit added it.                           |
| `after`                                                                              | [models.SubscriptionIntervalChangeCopy](../models/subscriptionintervalchangecopy.md) | :heavy_check_mark:                                                                   | The interval after the edit. Null when the edit removed it.                          |