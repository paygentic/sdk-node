# ListCostsResponse

List of costs

## Example Usage

```typescript
import { ListCostsResponse } from "@paygentic/sdk/models/operations";

let value: ListCostsResponse = {
  object: "list",
  data: [],
  pagination: {
    limit: 784022,
    offset: 957138,
    total: 725488,
  },
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `object`                                                                         | [operations.ListCostsObject](../../models/operations/listcostsobject.md)         | :heavy_check_mark:                                                               | N/A                                                                              |
| `data`                                                                           | [models.Cost](../../models/cost.md)[]                                            | :heavy_check_mark:                                                               | N/A                                                                              |
| `pagination`                                                                     | [operations.ListCostsPagination](../../models/operations/listcostspagination.md) | :heavy_check_mark:                                                               | N/A                                                                              |