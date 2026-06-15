# ListItemsResponse

List of items

## Example Usage

```typescript
import { ListItemsResponse } from "@paygentic/sdk/models/operations";

let value: ListItemsResponse = {
  data: [
    {
      id: "<id>",
      merchantId: "<id>",
      name: "<value>",
      metadata: {
        "key": "<value>",
      },
      externalReferences: [
        {
          id: "<id>",
          merchantId: "<id>",
          entityType: "customer",
          entityId: "<id>",
          provider: "<value>",
          externalId: "<id>",
          metadata: {
            "key": "<value>",
            "key1": "<value>",
            "key2": "<value>",
          },
          isPrimary: true,
          isDefault: true,
          createdAt: new Date("2025-07-31T11:07:44.107Z"),
          updatedAt: new Date("2026-04-23T20:22:22.390Z"),
        },
      ],
      createdAt: new Date("2024-09-13T00:54:15.007Z"),
      updatedAt: new Date("2025-12-05T05:12:41.970Z"),
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.Item](../../models/item.md)[]                       | :heavy_check_mark:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_check_mark:                                          | Offset-based pagination response.                           |