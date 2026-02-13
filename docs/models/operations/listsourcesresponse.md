# ListSourcesResponse

List of sources

## Example Usage

```typescript
import { ListSourcesResponse } from "@paygentic/sdk/models/operations";

let value: ListSourcesResponse = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.Source](../../models/source.md)[]                   | :heavy_minus_sign:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_minus_sign:                                          | Offset-based pagination response.                           |