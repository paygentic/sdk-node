# LineCalculationGiven

A value the evaluation started from, and its source.

## Example Usage

```typescript
import { LineCalculationGiven } from "@paygentic/sdk/models";

let value: LineCalculationGiven = {
  value: "<value>",
  source: "<value>",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `value`                                            | *string*                                           | :heavy_check_mark:                                 | The value.                                         |
| `source`                                           | *string*                                           | :heavy_check_mark:                                 | The key of the source in `sources` that stated it. |