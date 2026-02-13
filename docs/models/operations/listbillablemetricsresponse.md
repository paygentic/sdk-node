# ListBillableMetricsResponse

List of billable metrics

## Example Usage

```typescript
import { ListBillableMetricsResponse } from "@paygentic/sdk/models/operations";

let value: ListBillableMetricsResponse = {
  object: "list",
  data: [],
  pagination: {
    limit: 676914,
    offset: 331696,
    total: 149456,
  },
};
```

## Fields

| Field                                                                                                | Type                                                                                                 | Required                                                                                             | Description                                                                                          |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| `object`                                                                                             | [operations.ListBillableMetricsObject](../../models/operations/listbillablemetricsobject.md)         | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `data`                                                                                               | [models.BillableMetric](../../models/billablemetric.md)[]                                            | :heavy_check_mark:                                                                                   | N/A                                                                                                  |
| `pagination`                                                                                         | [operations.ListBillableMetricsPagination](../../models/operations/listbillablemetricspagination.md) | :heavy_check_mark:                                                                                   | N/A                                                                                                  |