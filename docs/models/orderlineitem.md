# OrderLineItem

## Example Usage

```typescript
import { OrderLineItem } from "@paygentic/sdk/models";

let value: OrderLineItem = {
  id: "<id>",
  object: "order_line_item",
  orderId: "<id>",
  quantity: "<value>",
  listUnitPrice: "<value>",
  discountUnitAmount: "<value>",
  unitPrice: "<value>",
  totalPrice: "<value>",
  termStartDate: null,
  termEndDate: new Date("2024-12-22T23:48:33.541Z"),
  metadata: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  createdAt: new Date("2024-08-22T07:46:29.812Z"),
  updatedAt: new Date("2026-02-02T05:02:47.422Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.OrderLineItemObject](../models/orderlineitemobject.md)                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `orderId`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `itemId`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `quantity`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string                                                                                |
| `listUnitPrice`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string                                                                                |
| `discountUnitAmount`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string                                                                                |
| `unitPrice`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string                                                                                |
| `totalPrice`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Decimal string                                                                                |
| `termStartDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `termEndDate`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |