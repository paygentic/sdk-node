# OffsetPagination

Offset-based pagination response.

## Example Usage

```typescript
import { OffsetPagination } from "@paygentic/sdk/models";

let value: OffsetPagination = {};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `limit`                                       | *number*                                      | :heavy_minus_sign:                            | Number of items returned in the current page. |
| `offset`                                      | *number*                                      | :heavy_minus_sign:                            | Number of items skipped.                      |
| `total`                                       | *number*                                      | :heavy_minus_sign:                            | Total number of items available.              |