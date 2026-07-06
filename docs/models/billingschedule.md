# BillingSchedule

Summary of a billing schedule owned by this order. The full schedule (with intervals + staged invoices) is served under /billingSchedules. Owner-polymorphic: a schedule belongs to exactly one Order or one Subscription (XOR); cadence lives on ScheduleIntervals, not the header.

## Example Usage

```typescript
import { BillingSchedule } from "@paygentic/sdk/models";

let value: BillingSchedule = {
  id: "<id>",
  object: "billing_schedule",
  merchantId: "<id>",
  status: "completed",
  startDate: new Date("2026-11-03T17:31:34.677Z"),
  endDate: new Date("2026-08-08T01:50:58.274Z"),
  billingAnchor: new Date("2026-03-05T16:26:46.664Z"),
  alignmentPolicy: "anchor",
  prorationPolicy: "daily",
  periodPreset: "P3M",
  metadata: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  createdAt: new Date("2026-11-28T17:30:10.850Z"),
  updatedAt: new Date("2024-05-29T16:30:09.149Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.BillingScheduleObject](../models/billingscheduleobject.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `orderId`                                                                                     | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `status`                                                                                      | [models.BillingScheduleStatus](../models/billingschedulestatus.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `startDate`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `endDate`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `billingAnchor`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `alignmentPolicy`                                                                             | [models.BillingScheduleAlignmentPolicy](../models/billingschedulealignmentpolicy.md)          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `prorationPolicy`                                                                             | [models.BillingScheduleProrationPolicy](../models/billingscheduleprorationpolicy.md)          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `paymentTermDays`                                                                             | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `periodPreset`                                                                                | [models.BillingSchedulePeriodPreset](../models/billingscheduleperiodpreset.md)                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |