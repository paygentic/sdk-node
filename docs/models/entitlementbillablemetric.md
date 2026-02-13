# EntitlementBillableMetric

## Example Usage

```typescript
import { EntitlementBillableMetric } from "@paygentic/sdk/models";

let value: EntitlementBillableMetric = {};
```

## Fields

| Field                                                                                                                                               | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `billableMetricId`                                                                                                                                  | *string*                                                                                                                                            | :heavy_minus_sign:                                                                                                                                  | Unique identifier for a billable metric                                                                                                             |
| `price`                                                                                                                                             | *string*                                                                                                                                            | :heavy_minus_sign:                                                                                                                                  | Custom price override in decimal dollars. Sample values: '0.000012' sets $0.000012 per unit, '0.50' sets $0.50 per unit, '1.25' sets $1.25 per unit |
| `quantity`                                                                                                                                          | *number*                                                                                                                                            | :heavy_minus_sign:                                                                                                                                  | Pre-authorized metric quantity amount. Sample values: 10000 tokens, 500 GB storage, 1000 API calls, 24 compute hours                                |