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
      },
      isPrimary: false,
      isDefault: true,
      createdAt: new Date("2024-04-26T00:59:15.058Z"),
      updatedAt: new Date("2025-07-31T11:07:44.107Z"),
    },
  ],
  createdAt: new Date("2026-04-23T20:22:22.390Z"),
  updatedAt: new Date("2024-07-08T04:24:00.354Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.ItemObject](../models/itemobject.md)                                                  | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `externalReferences`                                                                          | [models.ExternalReference](../models/externalreference.md)[]                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |