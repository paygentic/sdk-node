# PriceProperties4

Percentage pricing model

## Example Usage

```typescript
import { PriceProperties4 } from "@paygentic/sdk/models";

let value: PriceProperties4 = {
  maxCharge: "<value>",
  minCharge: "<value>",
  percentage: "<value>",
};
```

## Fields

| Field                                                                                                                                                                      | Type                                                                                                                                                                       | Required                                                                                                                                                                   | Description                                                                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `maxCharge`                                                                                                                                                                | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | Ceiling amount limiting total charge regardless of percentage calculation. Sample values: '500.00' caps fees at $500 maximum, '2000.00' limits charges to $2000 per period |
| `minCharge`                                                                                                                                                                | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | Floor amount charged regardless of percentage calculation. Sample values: '5.00' ensures minimum $5 fee, '25.00' guarantees at least $25 per billing event                 |
| `percentage`                                                                                                                                                               | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | Rate expressed as decimal between 0 and 10, supporting up to 4 decimal precision. Sample values: '0.03' represents 3%, '0.075' represents 7.5%, '1.10' represents 110%     |