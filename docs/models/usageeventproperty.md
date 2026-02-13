# UsageEventProperty

## Example Usage

```typescript
import { UsageEventProperty } from "@paygentic/sdk/models";

let value: UsageEventProperty = {
  billableMetricId: "<id>",
  quantity: 929498,
};
```

## Fields

| Field                                                                                                                                               | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `billableMetricId`                                                                                                                                  | *string*                                                                                                                                            | :heavy_check_mark:                                                                                                                                  | N/A                                                                                                                                                 |
| `price`                                                                                                                                             | *string*                                                                                                                                            | :heavy_minus_sign:                                                                                                                                  | Custom price override in decimal dollars. Sample values: '0.000012' sets $0.000012 per unit, '0.50' sets $0.50 per unit, '1.25' sets $1.25 per unit |
| `quantity`                                                                                                                                          | *number*                                                                                                                                            | :heavy_check_mark:                                                                                                                                  | Consumption quantity must be a positive whole number. Sample values: 1 for single unit, 100 for one hundred units, 2500 for tokens consumed         |