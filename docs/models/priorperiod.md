# PriorPeriod

Prior-period comparison data. Present only when comparePriorPeriod=true.

## Example Usage

```typescript
import { PriorPeriod } from "@paygentic/sdk/models";

let value: PriorPeriod = {
  cost: 5219.23,
  changePercent: 2238.78,
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `cost`                                                               | *number*                                                             | :heavy_check_mark:                                                   | N/A                                                                  |
| `changePercent`                                                      | *number*                                                             | :heavy_check_mark:                                                   | Percentage change vs prior period. Null when prior period cost is 0. |