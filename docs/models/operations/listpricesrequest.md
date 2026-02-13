# ListPricesRequest

## Example Usage

```typescript
import { ListPricesRequest } from "@paygentic/sdk/models/operations";

let value: ListPricesRequest = {};
```

## Fields

| Field                               | Type                                | Required                            | Description                         |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `billableMetricId`                  | *string*                            | :heavy_minus_sign:                  | Filter prices by billable metric ID |
| `limit`                             | *number*                            | :heavy_minus_sign:                  | Number of prices to return          |
| `offset`                            | *number*                            | :heavy_minus_sign:                  | Number of prices to skip            |