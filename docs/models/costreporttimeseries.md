# CostReportTimeSeries

## Example Usage

```typescript
import { CostReportTimeSeries } from "@paygentic/sdk/models";

let value: CostReportTimeSeries = {
  windowStart: new Date("2025-07-21T02:50:17.163Z"),
  windowEnd: new Date("2024-11-25T11:35:32.955Z"),
  groups: {
    "key": 7770.95,
    "key1": 4244.66,
    "key2": 4031.17,
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `windowStart`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `windowEnd`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `groups`                                                                                      | Record<string, *number*>                                                                      | :heavy_check_mark:                                                                            | Map of group key → cost value for this time window. Keys match CostReportGroup.key.           |