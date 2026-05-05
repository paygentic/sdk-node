# ListPaymentsResponse

List of payments

## Example Usage

```typescript
import { ListPaymentsResponse } from "@paygentic/sdk/models/operations";

let value: ListPaymentsResponse = {
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

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `object`                                                                       | [operations.ListPaymentsObject](../../models/operations/listpaymentsobject.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `data`                                                                         | [models.Payment](../../models/payment.md)[]                                    | :heavy_check_mark:                                                             | N/A                                                                            |
| `pagination`                                                                   | [models.OffsetPagination](../../models/offsetpagination.md)                    | :heavy_check_mark:                                                             | Offset-based pagination response.                                              |