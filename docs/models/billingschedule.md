# BillingSchedule

## Example Usage

```typescript
import { BillingSchedule } from "@paygentic/sdk/models";

let value: BillingSchedule = {
  id: "<id>",
  object: "billing_schedule",
  merchantId: "<id>",
  status: "completed",
  startDate: new Date("2026-11-03T17:31:34.677Z"),
  endDate: new Date("2026-03-05T16:26:46.664Z"),
  billingAnchor: new Date("2024-10-24T08:50:07.303Z"),
  alignmentPolicy: "calendar",
  prorationPolicy: "none",
  periodPreset: "P1Y",
  customPeriodWindows: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  metadata: {},
  createdAt: new Date("2025-05-08T20:31:33.616Z"),
  updatedAt: new Date("2026-04-28T18:05:18.829Z"),
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
| `endDate`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | The schedule's end date. Always present.                                                      |
| `billingAnchor`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `alignmentPolicy`                                                                             | [models.BillingScheduleAlignmentPolicy](../models/billingschedulealignmentpolicy.md)          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `prorationPolicy`                                                                             | [models.BillingScheduleProrationPolicy](../models/billingscheduleprorationpolicy.md)          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `paymentTermDays`                                                                             | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `periodPreset`                                                                                | [models.BillingSchedulePeriodPreset](../models/billingscheduleperiodpreset.md)                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `customPeriodWindows`                                                                         | *any*[]                                                                                       | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `deletedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |