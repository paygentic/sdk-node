# SchemasBillingSchedule

## Example Usage

```typescript
import { SchemasBillingSchedule } from "@paygentic/sdk/models";

let value: SchemasBillingSchedule = {
  id: "<id>",
  object: "billing_schedule",
  merchantId: "<id>",
  status: "completed",
  startDate: new Date("2024-09-19T09:54:21.530Z"),
  endDate: new Date("2026-10-23T16:16:34.786Z"),
  billingAnchor: new Date("2024-08-11T22:03:12.097Z"),
  alignmentPolicy: "anchor",
  prorationPolicy: "daily",
  periodPreset: "P1Y",
  customPeriodWindows: [
    "<value 1>",
  ],
  metadata: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  createdAt: new Date("2025-07-31T11:29:30.742Z"),
  updatedAt: new Date("2024-05-11T04:08:35.500Z"),
};
```

## Fields

| Field                                                                                                 | Type                                                                                                  | Required                                                                                              | Description                                                                                           |
| ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| `id`                                                                                                  | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `object`                                                                                              | [models.SchemasBillingScheduleObject](../models/schemasbillingscheduleobject.md)                      | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `orderId`                                                                                             | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `subscriptionId`                                                                                      | *string*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `merchantId`                                                                                          | *string*                                                                                              | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `status`                                                                                              | [models.SchemasBillingScheduleStatus](../models/schemasbillingschedulestatus.md)                      | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `startDate`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `endDate`                                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | Null for an open-ended subscription-owned schedule; order-owned schedules always have a concrete end. |
| `billingAnchor`                                                                                       | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `alignmentPolicy`                                                                                     | [models.SchemasBillingScheduleAlignmentPolicy](../models/schemasbillingschedulealignmentpolicy.md)    | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `prorationPolicy`                                                                                     | [models.SchemasBillingScheduleProrationPolicy](../models/schemasbillingscheduleprorationpolicy.md)    | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `paymentTermDays`                                                                                     | *number*                                                                                              | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |
| `periodPreset`                                                                                        | [models.SchemasBillingSchedulePeriodPreset](../models/schemasbillingscheduleperiodpreset.md)          | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `customPeriodWindows`                                                                                 | *any*[]                                                                                               | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `metadata`                                                                                            | Record<string, *any*>                                                                                 | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `createdAt`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `updatedAt`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_check_mark:                                                                                    | N/A                                                                                                   |
| `deletedAt`                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)         | :heavy_minus_sign:                                                                                    | N/A                                                                                                   |