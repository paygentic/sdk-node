# ScheduleInterval

## Example Usage

```typescript
import { ScheduleInterval } from "@paygentic/sdk/models";

let value: ScheduleInterval = {
  id: "<id>",
  object: "schedule_interval",
  scheduleId: "<id>",
  baseQuantity: "<value>",
  quantityTransitions: [
    {
      effectiveDate: new Date("2024-08-14T01:05:01.893Z"),
      quantity: "<value>",
    },
  ],
  billingCadence: "<value>",
  billingMode: "arrears",
  startDate: new Date("2026-11-20T06:22:46.100Z"),
  endDate: new Date("2026-12-25T22:49:58.842Z"),
  metadata: {},
  createdAt: new Date("2024-05-03T11:55:56.758Z"),
  updatedAt: new Date("2024-04-13T16:10:42.172Z"),
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `id`                                                                                                  | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `object`                                                                                              | [models.ScheduleIntervalObject](../models/scheduleintervalobject.md)                                  | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `scheduleId`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `orderLineItemId`                                                                                     | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `itemId`                                                                                              | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `priceId`                                                                                             | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `description`                                                                                         | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `unitPrice`                                                                                           | *string*                                                                                              | :heavy_minus_sign:                                                                                    | Signed per-period net unit price as decimal string                                                    |
| `baseQuantity`                                                                                        | *string*                                                                                              | :heavy_check_mark:                                                                                    | Quantity at interval start                                                                            |
| `quantityTransitions`                                                                                 | [models.ScheduleIntervalQuantityTransition](../models/scheduleintervalquantitytransition.md)[]        | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `billingCadence`                                                                                      | *string*                                                                                              | :heavy_check_mark:                                                                                    | ISO-8601 duration or 'one_off'                                                                        |
| `billingMode`                                                                                         | [models.ScheduleIntervalBillingMode](../models/scheduleintervalbillingmode.md)                        | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `billDate`                                                                                            | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `startDate`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `endDate`                                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | Null for an open-ended subscription-owned interval; order-owned intervals always have a concrete end. |
| `usageFilter`                                                                                         | Record<string, *any*>                                                                                 | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `metadata`                                                                                            | Record<string, *any*>                                                                                 | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `createdAt`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `updatedAt`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |