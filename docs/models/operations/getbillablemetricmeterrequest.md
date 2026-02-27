# GetBillableMetricMeterRequest

## Example Usage

```typescript
import { GetBillableMetricMeterRequest } from "@paygentic/sdk/models/operations";

let value: GetBillableMetricMeterRequest = {
  id: "<id>",
  from: new Date("2025-01-28T19:31:41.633Z"),
  to: new Date("2025-10-03T07:59:23.144Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Start of query window (ISO 8601)                                                              |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | End of query window (ISO 8601)                                                                |
| `subject`                                                                                     | *string*                                                                                      | :heavy_minus_sign:                                                                            | Filter by customer/user ID                                                                    |
| `windowSize`                                                                                  | [operations.WindowSize](../../models/operations/windowsize.md)                                | :heavy_minus_sign:                                                                            | Time bucket granularity                                                                       |
| `filterGroupBy`                                                                               | *string*                                                                                      | :heavy_minus_sign:                                                                            | JSON-encoded dimension filter (e.g. {"key":"value"})                                          |
| `groupBy`                                                                                     | *string*                                                                                      | :heavy_minus_sign:                                                                            | Comma-separated dimension keys                                                                |