# ListFeaturesPagination

## Example Usage

```typescript
import { ListFeaturesPagination } from "@paygentic/sdk/models/operations";

let value: ListFeaturesPagination = {
  limit: 373340,
  offset: 516447,
  total: 348882,
};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `limit`                                  | *number*                                 | :heavy_check_mark:                       | Number of items requested                |
| `offset`                                 | *number*                                 | :heavy_check_mark:                       | Number of items skipped                  |
| `total`                                  | *number*                                 | :heavy_check_mark:                       | Total number of items matching the query |