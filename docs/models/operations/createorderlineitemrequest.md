# CreateOrderLineItemRequest

## Example Usage

```typescript
import { CreateOrderLineItemRequest } from "@paygentic/sdk/models/operations";

let value: CreateOrderLineItemRequest = {
  orderId: "<id>",
  createOrderLineItemRequest: {
    quantity: "<value>",
    listUnitPrice: "<value>",
    unitPrice: "<value>",
    totalPrice: "<value>",
  },
};
```

## Fields

| Field                                                                           | Type                                                                            | Required                                                                        | Description                                                                     |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| `orderId`                                                                       | *string*                                                                        | :heavy_check_mark:                                                              | N/A                                                                             |
| `createOrderLineItemRequest`                                                    | [models.CreateOrderLineItemRequest](../../models/createorderlineitemrequest.md) | :heavy_check_mark:                                                              | N/A                                                                             |