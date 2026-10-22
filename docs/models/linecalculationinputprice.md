# LineCalculationInputPrice

`priced` only: the price as a function, and its source.

## Example Usage

```typescript
import { LineCalculationInputPrice } from "@paygentic/sdk/models";

let value: LineCalculationInputPrice = {
  fn: {
    model: "Challenger",
  },
  source: "<value>",
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `fn`                                                                                        | [models.LineCalculationPriceFn](../models/linecalculationpricefn.md)                        | :heavy_check_mark:                                                                          | A price as a function from quantity to money. A new model may carry fields not listed here. |
| `source`                                                                                    | *string*                                                                                    | :heavy_check_mark:                                                                          | The key of the source in `sources` that stated the price.                                   |