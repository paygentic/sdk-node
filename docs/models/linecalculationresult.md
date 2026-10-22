# LineCalculationResult

Equal to the line's stored amount, quantity and unit price.

## Example Usage

```typescript
import { LineCalculationResult } from "@paygentic/sdk/models";

let value: LineCalculationResult = {
  amount: "203.88",
  quantity: null,
  unitPrice: "<value>",
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `amount`                                                                                           | *string*                                                                                           | :heavy_check_mark:                                                                                 | The line's amount before tax.                                                                      |
| `quantity`                                                                                         | *string*                                                                                           | :heavy_check_mark:                                                                                 | The line's quantity.                                                                               |
| `unitPrice`                                                                                        | *string*                                                                                           | :heavy_check_mark:                                                                                 | The line's unit price. It can be rounded, so quantity times unit price can differ from the amount. |