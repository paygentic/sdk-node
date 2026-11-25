# ListPricingUnitsResponse

List of pricing units

## Example Usage

```typescript
import { ListPricingUnitsResponse } from "@paygentic/sdk/models/operations";

let value: ListPricingUnitsResponse = {
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
| `data`                                                      | [models.PricingUnit](../../models/pricingunit.md)[]         | :heavy_check_mark:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_check_mark:                                          | Offset-based pagination response.                           |