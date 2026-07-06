# ScheduleInvoice

## Example Usage

```typescript
import { ScheduleInvoice } from "@paygentic/sdk/models";

let value: ScheduleInvoice = {
  id: "<id>",
  object: "schedule_invoice",
  orderId: "<id>",
  billingScheduleId: "<id>",
  merchantId: "<id>",
  periodStart: new Date("2024-07-15T06:19:48.857Z"),
  periodEnd: new Date("2025-09-12T18:41:15.025Z"),
  dueDate: new Date("2024-06-15T21:35:12.415Z"),
  amount: "946.03",
  status: "pushed",
  lineItems: [],
  createdAt: new Date("2024-12-28T14:07:32.678Z"),
  updatedAt: new Date("2025-07-19T05:56:09.599Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.ScheduleInvoiceObject](../models/scheduleinvoiceobject.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `orderId`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `billingScheduleId`                                                                           | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `periodStart`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `periodEnd`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `dueDate`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `amount`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Net invoice amount as decimal string                                                          |
| `status`                                                                                      | [models.ScheduleInvoiceStatus](../models/scheduleinvoicestatus.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `lineItems`                                                                                   | [models.ScheduleInvoiceLineItem](../models/scheduleinvoicelineitem.md)[]                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |