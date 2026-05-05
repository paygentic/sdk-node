# ProfitabilityTrend

## Example Usage

```typescript
import { ProfitabilityTrend } from "@paygentic/sdk/models";

let value: ProfitabilityTrend = {
  values: [
    "<value 1>",
  ],
  periodChange: 9003.94,
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `values`                                                                           | *string*[]                                                                         | :heavy_check_mark:                                                                 | Revenue values per time bucket, oldest first, in unit currency with two decimals.  |
| `periodChange`                                                                     | *number*                                                                           | :heavy_check_mark:                                                                 | Period-over-period % change (current half vs prior half). Null when prior is zero. |