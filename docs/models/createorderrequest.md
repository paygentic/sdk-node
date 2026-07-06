# CreateOrderRequest

## Example Usage

```typescript
import { CreateOrderRequest } from "@paygentic/sdk/models";

let value: CreateOrderRequest = {
  customerId: "<id>",
  currency: "Som",
  termStartDate: new Date("2026-12-24T09:35:43.459Z"),
  termEndDate: new Date("2026-09-17T04:44:55.016Z"),
  totalAmount: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.CreateOrderRequestType](../models/createorderrequesttype.md)                          | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `termStartDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `termEndDate`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `closeDate`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `totalAmount`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `defaultPaymentTermDays`                                                                      | *number*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `lineItems`                                                                                   | [models.CreateOrderLineItemRequest](../models/createorderlineitemrequest.md)[]                | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `resellerId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `taxExempt`                                                                                   | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `sellingEntity`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |