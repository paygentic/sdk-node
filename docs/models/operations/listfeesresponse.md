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
      createdAt: new Date("2026-09-26T20:50:14.986Z"),
      updatedAt: new Date("2024-04-13T08:30:31.889Z"),
    },
  ],
  pagination: {
    limit: 427428,
    offset: 742322,
    total: 297500,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [operations.ListFeesObject](../../models/operations/listfeesobject.md)         | :heavy_check_mark:                                                             | N/A                                                                            |
| `data`                                                                         | [models.Fee](../../models/fee.md)[]                                            | :heavy_check_mark:                                                             | N/A                                                                            |
| `pagination`                                                                   | [operations.ListFeesPagination](../../models/operations/listfeespagination.md) | :heavy_check_mark:                                                             | N/A                                                                            |