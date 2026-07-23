# ListPlanVersionsResponse

List of plan versions

## Example Usage

```typescript
import { ListPlanVersionsResponse } from "@paygentic/sdk/models/operations";

let value: ListPlanVersionsResponse = {
  object: "list",
  data: [
    {
      id: "<id>",
      object: "plan_version",
      versionNumber: 572508,
      status: "published",
      isDefault: false,
      subscriptionCount: 87647,
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `object`                                                                               | [operations.ListPlanVersionsObject](../../models/operations/listplanversionsobject.md) | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `data`                                                                                 | [models.PlanVersionSummary](../../models/planversionsummary.md)[]                      | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `pagination`                                                                           | [models.OffsetPagination](../../models/offsetpagination.md)                            | :heavy_check_mark:                                                                     | Offset-based pagination response.                                                      |