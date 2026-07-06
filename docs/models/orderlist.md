# OrderList

## Example Usage

```typescript
import { OrderList } from "@paygentic/sdk/models";

let value: OrderList = {
  object: "list",
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `object`                                                 | [models.OrderListObject](../models/orderlistobject.md)   | :heavy_check_mark:                                       | N/A                                                      |
| `data`                                                   | [models.Order](../models/order.md)[]                     | :heavy_check_mark:                                       | N/A                                                      |
| `pagination`                                             | [models.OffsetPagination](../models/offsetpagination.md) | :heavy_check_mark:                                       | Offset-based pagination response.                        |