# ListBillableMetricEventsRequest

## Example Usage

```typescript
import { ListBillableMetricEventsRequest } from "@paygentic/sdk/models/operations";

let value: ListBillableMetricEventsRequest = {
  id: "<id>",
  from: new Date("2025-03-27T19:48:58.427Z"),
  to: new Date("2025-07-02T21:22:41.406Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Start of query window (ISO 8601)                                                              |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | End of query window (ISO 8601)                                                                |
| `subject`                                                                                     | *string*                                                                                      | :heavy_minus_sign:                                                                            | Filter by subject (typically the customer/user ID)                                            |
| `limit`                                                                                       | *number*                                                                                      | :heavy_minus_sign:                                                                            | Maximum number of events to return                                                            |
| `offset`                                                                                      | *number*                                                                                      | :heavy_minus_sign:                                                                            | Number of events to skip                                                                      |
| `externalId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | Filter by external identifier. Alphanumeric characters, hyphens, and underscores only.        |