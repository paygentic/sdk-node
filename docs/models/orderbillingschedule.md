# OrderBillingSchedule

Summary of a billing schedule owned by this order. The full schedule (with intervals + staged invoices) is served under /billingSchedules. Owner-polymorphic: a schedule belongs to exactly one Order or one Subscription (XOR); cadence lives on ScheduleIntervals, not the header.

## Example Usage

```typescript
import { OrderBillingSchedule } from "@paygentic/sdk/models";

let value: OrderBillingSchedule = {
  id: "<id>",
  object: "billing_schedule",
  merchantId: "<id>",
  status: "cancelled",
  startDate: new Date("2024-09-10T02:20:15.079Z"),
  endDate: new Date("2026-10-13T15:26:04.802Z"),
  billingAnchor: new Date("2024-08-21T23:14:05.693Z"),
  alignmentPolicy: "calendar",
  prorationPolicy: "daily",
  periodPreset: "P1M",
  metadata: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  createdAt: new Date("2024-05-11T17:35:08.288Z"),
  updatedAt: new Date("2025-02-08T19:49:18.849Z"),
};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `id`                                                                                           | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `object`                                                                                       | [models.OrderBillingScheduleObject](../models/orderbillingscheduleobject.md)                   | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `orderId`                                                                                      | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `subscriptionId`                                                                               | *string*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `merchantId`                                                                                   | *string*                                                                                       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `status`                                                                                       | [models.OrderBillingScheduleStatus](../models/orderbillingschedulestatus.md)                   | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `startDate`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)  | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `endDate`                                                                                      | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)  | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `billingAnchor`                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)  | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `alignmentPolicy`                                                                              | [models.OrderBillingScheduleAlignmentPolicy](../models/orderbillingschedulealignmentpolicy.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `prorationPolicy`                                                                              | [models.OrderBillingScheduleProrationPolicy](../models/orderbillingscheduleprorationpolicy.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `paymentTermDays`                                                                              | *number*                                                                                       | :heavy_minus_sign:                                                                             | N/A                                                                                            |
| `periodPreset`                                                                                 | [models.OrderBillingSchedulePeriodPreset](../models/orderbillingscheduleperiodpreset.md)       | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `metadata`                                                                                     | Record<string, *any*>                                                                          | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `createdAt`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)  | :heavy_check_mark:                                                                             | N/A                                                                                            |
| `updatedAt`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)  | :heavy_check_mark:                                                                             | N/A                                                                                            |