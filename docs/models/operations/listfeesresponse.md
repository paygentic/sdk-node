# ListFeesResponse

List of fees

## Example Usage

```typescript
import { ListFeesResponse } from "@paygentic/sdk/models/operations";

let value: ListFeesResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      name: "<value>",
      description: "since while ah why illusion regularly adventurously",
      merchantId: "<id>",
      productId: "<id>",
      itemId: "<id>",
      createdAt: new Date("2024-04-13T08:30:31.889Z"),
      updatedAt: new Date("2025-04-13T11:04:42.548Z"),
    },
  ],
  pagination: {
    limit: 742322,
    offset: 297500,
    total: 528685,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [operations.ListFeesObject](../../models/operations/listfeesobject.md)         | :heavy_check_mark:                                                             | N/A                                                                            |
| `data`                                                                         | [models.Fee](../../models/fee.md)[]                                            | :heavy_check_mark:                                                             | N/A                                                                            |
| `pagination`                                                                   | [operations.ListFeesPagination](../../models/operations/listfeespagination.md) | :heavy_check_mark:                                                             | N/A                                                                            |