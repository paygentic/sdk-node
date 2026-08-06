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
          entityType: "item",
          entityId: "<id>",
          provider: "<value>",
          externalId: "<id>",
          metadata: {
            "key": "<value>",
            "key1": "<value>",
            "key2": "<value>",
          },
          isPrimary: true,
          isDefault: false,
          createdAt: new Date("2024-02-18T18:56:41.548Z"),
          updatedAt: new Date("2025-01-29T02:39:26.489Z"),
        },
      ],
      catalogId: "<id>",
      archivedAt: new Date("2024-05-23T01:31:17.998Z"),
      createdAt: new Date("2024-05-13T18:53:13.139Z"),
      updatedAt: new Date("2025-05-27T07:48:56.222Z"),
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