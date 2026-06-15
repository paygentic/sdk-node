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
  createdAt: new Date("2024-07-08T04:24:00.354Z"),
  updatedAt: new Date("2026-12-15T02:58:19.832Z"),
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