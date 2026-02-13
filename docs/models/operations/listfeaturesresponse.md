# ListFeaturesResponse

List of features

## Example Usage

```typescript
import { ListFeaturesResponse } from "@paygentic/sdk/models/operations";

let value: ListFeaturesResponse = {
  object: "list",
  data: [],
  pagination: {
    limit: 687370,
    offset: 305090,
    total: 11085,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `object`                                                                               | [operations.ListFeaturesObject](../../models/operations/listfeaturesobject.md)         | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `data`                                                                                 | [models.Feature](../../models/feature.md)[]                                            | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pagination`                                                                           | [operations.ListFeaturesPagination](../../models/operations/listfeaturespagination.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |