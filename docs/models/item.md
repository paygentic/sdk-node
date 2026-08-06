# Item

## Example Usage

```typescript
import { Item } from "@paygentic/sdk/models";

let value: Item = {
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
  archivedAt: new Date("2025-01-31T04:17:37.835Z"),
  createdAt: new Date("2024-04-26T00:59:15.058Z"),
  updatedAt: new Date("2025-07-31T11:07:44.107Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an item                                                                 |
| `object`                                                                                      | [models.ItemObject](../models/itemobject.md)                                                  | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `externalReferences`                                                                          | [models.ExternalReference](../models/externalreference.md)[]                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `catalogId`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | The product this item belongs to.                                                             |
| `archivedAt`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When this item was retired from the catalog. Null while active.                               |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |