# ListExternalReferencesResponse

List of external references

## Example Usage

```typescript
import { ListExternalReferencesResponse } from "@paygentic/sdk/models/operations";

let value: ListExternalReferencesResponse = {
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `data`                                                          | [models.ExternalReference](../../models/externalreference.md)[] | :heavy_check_mark:                                              | N/A                                                             |
| `pagination`                                                    | [models.OffsetPagination](../../models/offsetpagination.md)     | :heavy_check_mark:                                              | Offset-based pagination response.                               |