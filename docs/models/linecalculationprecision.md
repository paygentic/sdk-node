# LineCalculationPrecision

The default arithmetic of every step. Any other rounding is an explicit `round` step.

## Example Usage

```typescript
import { LineCalculationPrecision } from "@paygentic/sdk/models";

let value: LineCalculationPrecision = {
  significantDigits: 490055,
  rounding: "<value>",
};
```

## Fields

| Field               | Type                | Required            | Description         |
| ------------------- | ------------------- | ------------------- | ------------------- |
| `significantDigits` | *number*            | :heavy_check_mark:  | N/A                 |
| `rounding`          | *string*            | :heavy_check_mark:  | N/A                 |