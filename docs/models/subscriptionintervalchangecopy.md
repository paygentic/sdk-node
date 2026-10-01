# SubscriptionIntervalChangeCopy

What an interval billed at one point in time.

## Example Usage

```typescript
import { SubscriptionIntervalChangeCopy } from "@paygentic/sdk/models";

let value: SubscriptionIntervalChangeCopy = {
  priceId: "<id>",
  priceKey: "<value>",
  planVersionId: "<id>",
  unitPrice: "<value>",
  resolvedUnitPrice: "<value>",
  baseQuantity: "<value>",
  quantityTransitions: [],
  billingCadence: "<value>",
  billingMode: "advance",
  billDate: new Date("2024-12-02T09:35:31.530Z"),
  startDate: new Date("2025-12-09T20:36:04.835Z"),
  endDate: new Date("2024-06-18T02:05:00.049Z"),
};
```

## Fields

| Field                                                                                                                      | Type                                                                                                                       | Required                                                                                                                   | Description                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `priceId`                                                                                                                  | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `priceKey`                                                                                                                 | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `planVersionId`                                                                                                            | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | The plan version the interval belongs to.                                                                                  |
| `unitPrice`                                                                                                                | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | The rate as a decimal string, or null when the interval bills the catalog rate.                                            |
| `resolvedUnitPrice`                                                                                                        | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | The per-unit rate the interval charged when the change was made.                                                           |
| `baseQuantity`                                                                                                             | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `quantityTransitions`                                                                                                      | [models.SubscriptionIntervalChangeCopyQuantityTransition](../models/subscriptionintervalchangecopyquantitytransition.md)[] | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `billingCadence`                                                                                                           | *string*                                                                                                                   | :heavy_check_mark:                                                                                                         | ISO-8601 duration or 'one_off'                                                                                             |
| `billingMode`                                                                                                              | [models.SubscriptionIntervalChangeCopyBillingMode](../models/subscriptionintervalchangecopybillingmode.md)                 | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `billDate`                                                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                              | :heavy_check_mark:                                                                                                         | When a one-off interval bills. Null for every other cadence.                                                               |
| `startDate`                                                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                              | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |
| `endDate`                                                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                              | :heavy_check_mark:                                                                                                         | N/A                                                                                                                        |