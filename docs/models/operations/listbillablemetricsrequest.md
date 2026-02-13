# ListBillableMetricsRequest

## Example Usage

```typescript
import { ListBillableMetricsRequest } from "@paygentic/sdk/models/operations";

let value: ListBillableMetricsRequest = {
  merchantId: "<id>",
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `limit`                                              | *number*                                             | :heavy_minus_sign:                                   | Number of billable metrics to return.                |
| `merchantId`                                         | *string*                                             | :heavy_check_mark:                                   | Filter billable metrics by merchant organization ID. |
| `offset`                                             | *number*                                             | :heavy_minus_sign:                                   | Number of billable metrics to skip.                  |
| `productId`                                          | *string*                                             | :heavy_minus_sign:                                   | Filter billable metrics by product ID.               |