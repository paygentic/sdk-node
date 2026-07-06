# Order

## Example Usage

```typescript
import { Order } from "@paygentic/sdk/models";

let value: Order = {
  id: "<id>",
  object: "order",
  merchantId: "<id>",
  customerId: "<id>",
  resellerId: "<id>",
  taxExempt: true,
  sellingEntity: "<value>",
  currency: "Taka",
  approvalStatus: "pending",
  cancelledAt: new Date("2026-05-22T09:42:18.020Z"),
  termStartDate: new Date("2025-03-04T09:04:40.951Z"),
  termEndDate: new Date("2026-08-04T13:01:16.646Z"),
  totalAmount: "<value>",
  defaultPaymentTermDays: 250136,
  metadata: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  lineItems: [],
  billingSchedules: [
    {
      id: "<id>",
      object: "billing_schedule",
      merchantId: "<id>",
      status: "draft",
      startDate: new Date("2025-01-30T19:32:56.423Z"),
      endDate: new Date("2025-09-09T17:35:57.049Z"),
      billingAnchor: new Date("2025-02-15T11:18:39.347Z"),
      alignmentPolicy: "calendar",
      prorationPolicy: "none",
      periodPreset: "single",
      metadata: {},
      createdAt: new Date("2024-03-01T02:03:14.124Z"),
      updatedAt: new Date("2024-10-23T00:55:41.034Z"),
    },
  ],
  createdAt: new Date("2026-02-02T20:35:02.495Z"),
  updatedAt: new Date("2026-09-26T23:45:02.094Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.OrderObject](../models/orderobject.md)                                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `resellerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `taxExempt`                                                                                   | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `sellingEntity`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `approvalStatus`                                                                              | [models.ApprovalStatus](../models/approvalstatus.md)                                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `cancelledAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.OrderType](../models/ordertype.md)                                                    | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `termStartDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `termEndDate`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `closeDate`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `totalAmount`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string (TCV)                                                                          |
| `defaultPaymentTermDays`                                                                      | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `lineItems`                                                                                   | [models.OrderLineItem](../models/orderlineitem.md)[]                                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `billingSchedules`                                                                            | [models.BillingSchedule](../models/billingschedule.md)[]                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |