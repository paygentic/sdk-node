# OffsetPagination

Offset-based pagination response.

## Example Usage

```typescript
import { OffsetPagination } from "@paygentic/sdk/models";

let value: OffsetPagination = {
  limit: 170159,
  offset: 841082,
  total: 168759,
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `limit`                          | *number*                         | :heavy_check_mark:               | Requested page size.             |
| `offset`                         | *number*                         | :heavy_check_mark:               | Number of items skipped.         |
| `total`                          | *number*                         | :heavy_check_mark:               | Total number of items available. |