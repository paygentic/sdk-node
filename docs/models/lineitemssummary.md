# LineItemsSummary

## Example Usage

```typescript
import { LineItemsSummary } from "@paygentic/sdk/models";

let value: LineItemsSummary = {
  feeSubtotal: "<value>",
  meteredEstimatedSubtotal: "<value>",
  currency: "Tugrik",
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `feeSubtotal`                                           | *string*                                                | :heavy_check_mark:                                      | Sum of fee items with known subtotals in decimal format |
| `meteredEstimatedSubtotal`                              | *string*                                                | :heavy_check_mark:                                      | Sum of estimated metered amounts in decimal format      |
| `currency`                                              | *string*                                                | :heavy_check_mark:                                      | ISO 4217 currency code                                  |