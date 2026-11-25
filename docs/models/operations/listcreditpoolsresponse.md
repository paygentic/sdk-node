# ListCreditPoolsResponse

List of credit pools

## Example Usage

```typescript
import { ListCreditPoolsResponse } from "@paygentic/sdk/models/operations";

let value: ListCreditPoolsResponse = {
  data: [],
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
| `data`                                                      | [models.CreditPool](../../models/creditpool.md)[]           | :heavy_check_mark:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_check_mark:                                          | Offset-based pagination response.                           |