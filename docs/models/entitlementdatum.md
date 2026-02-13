# EntitlementDatum

## Example Usage

```typescript
import { EntitlementDatum } from "@paygentic/sdk/models";

let value: EntitlementDatum = {
  billableMetricId: "<id>",
  quantity: 2763.89,
};
```

## Fields

| Field                                                                                                                                                       | Type                                                                                                                                                        | Required                                                                                                                                                    | Description                                                                                                                                                 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `billableMetricId`                                                                                                                                          | *string*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | Unique identifier for a billable metric                                                                                                                     |
| `price`                                                                                                                                                     | *string*                                                                                                                                                    | :heavy_minus_sign:                                                                                                                                          | Optional per-unit price override in decimal dollars for variable-rate pricing. Sample values: '0.000025' sets $0.000025 per token, '0.12' sets $0.12 per GB |
| `quantity`                                                                                                                                                  | *number*                                                                                                                                                    | :heavy_check_mark:                                                                                                                                          | Amount of metric units to pre-authorize. Sample values: 10000 tokens, 500 GB storage, 1000 API calls, 24 compute hours                                      |