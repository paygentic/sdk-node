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
  endDate: new Date("2026-07-27T07:39:19.996Z"),
  billingAnchor: new Date("2026-10-23T16:16:34.786Z"),
  alignmentPolicy: "anchor",
  prorationPolicy: "none",
  periodPreset: "P6M",
  customPeriodWindows: [
    "<value 1>",
    "<value 2>",
  ],
  metadata: {
    "key": "<value>",
  },
  createdAt: new Date("2026-11-09T01:47:12.017Z"),
  updatedAt: new Date("2025-07-31T11:29:30.742Z"),
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `id`                                                                                               | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `object`                                                                                           | [models.SchemasBillingScheduleObject](../models/schemasbillingscheduleobject.md)                   | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `orderId`                                                                                          | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `subscriptionId`                                                                                   | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `merchantId`                                                                                       | *string*                                                                                           | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `status`                                                                                           | [models.SchemasBillingScheduleStatus](../models/schemasbillingschedulestatus.md)                   | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `startDate`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `endDate`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `billingAnchor`                                                                                    | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `alignmentPolicy`                                                                                  | [models.SchemasBillingScheduleAlignmentPolicy](../models/schemasbillingschedulealignmentpolicy.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `prorationPolicy`                                                                                  | [models.SchemasBillingScheduleProrationPolicy](../models/schemasbillingscheduleprorationpolicy.md) | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `paymentTermDays`                                                                                  | *number*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |
| `periodPreset`                                                                                     | [models.SchemasBillingSchedulePeriodPreset](../models/schemasbillingscheduleperiodpreset.md)       | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `customPeriodWindows`                                                                              | *any*[]                                                                                            | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `metadata`                                                                                         | Record<string, *any*>                                                                              | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `createdAt`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `updatedAt`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_check_mark:                                                                                 | N/A                                                                                                |
| `deletedAt`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)      | :heavy_minus_sign:                                                                                 | N/A                                                                                                |