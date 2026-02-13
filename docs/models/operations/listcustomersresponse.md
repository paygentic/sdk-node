# ListCustomersResponse

List of customers retrieved successfully

## Example Usage

```typescript
import { ListCustomersResponse } from "@paygentic/sdk/models/operations";

let value: ListCustomersResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      consumerId: "<id>",
      createdAt: new Date("2026-01-17T05:17:22.855Z"),
      merchantId: "<id>",
      updatedAt: new Date("2024-10-29T09:44:44.810Z"),
      validTaxAddress: {
        valid: false,
      },
    },
  ],
  pagination: {},
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `object`                                                                         | [operations.ListCustomersObject](../../models/operations/listcustomersobject.md) | :heavy_check_mark:                                                               | N/A                                                                              |
| `data`                                                                           | [models.Customer](../../models/customer.md)[]                                    | :heavy_check_mark:                                                               | N/A                                                                              |
| `pagination`                                                                     | [models.OffsetPagination](../../models/offsetpagination.md)                      | :heavy_check_mark:                                                               | Offset-based pagination response.                                                |