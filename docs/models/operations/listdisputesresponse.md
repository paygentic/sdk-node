# ListDisputesResponse

Disputes retrieved successfully

## Example Usage

```typescript
import { ListDisputesResponse } from "@paygentic/sdk/models/operations";
import { Decimal } from "@paygentic/sdk/types";

let value: ListDisputesResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      createdAt: new Date("2026-01-01T09:33:20.160Z"),
      customerId: "<id>",
      customerMessage: "<value>",
      disputedAmount: new Decimal("5427.92"),
      merchantId: "<id>",
      status: "declined",
      updatedAt: new Date("2024-12-21T07:58:17.948Z"),
      usageEventId: "<id>",
      customer: {
        id: "<id>",
        email: "Janelle_Heaney84@gmail.com",
        name: "<value>",
      },
    },
  ],
  pagination: {
    limit: 627160,
    offset: 231745,
    total: 859120,
    hasMore: true,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `object`                                                                               | [operations.ListDisputesObject](../../models/operations/listdisputesobject.md)         | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `data`                                                                                 | [models.DisputeWithCustomer](../../models/disputewithcustomer.md)[]                    | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pagination`                                                                           | [operations.ListDisputesPagination](../../models/operations/listdisputespagination.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |