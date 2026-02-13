# GetRevenueRequest

## Example Usage

```typescript
import { GetRevenueRequest } from "@paygentic/sdk/models/operations";

let value: GetRevenueRequest = {
  startTime: new Date("2024-06-09T16:55:34.271Z"),
  endTime: new Date("2026-05-23T20:41:02.411Z"),
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `startTime`                                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)            | :heavy_check_mark:                                                                                       | Start of the time range (ISO 8601 format)                                                                |
| `endTime`                                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)            | :heavy_check_mark:                                                                                       | End of the time range (ISO 8601 format)                                                                  |
| `bucketWidth`                                                                                            | [operations.BucketWidth](../../models/operations/bucketwidth.md)                                         | :heavy_minus_sign:                                                                                       | Time bucket granularity                                                                                  |
| `merchantId`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Filter by merchant ID. At least one of merchantId, subscriptionIds, or customerId must be provided.      |
| `customerId`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | Filter by customer ID. At least one of merchantId, subscriptionIds, or customerId must be provided.      |
| `subscriptionIds`                                                                                        | *string*[]                                                                                               | :heavy_minus_sign:                                                                                       | Filter by subscription IDs. At least one of merchantId, subscriptionIds, or customerId must be provided. |
| `topN`                                                                                                   | *number*                                                                                                 | :heavy_minus_sign:                                                                                       | Limit to top N subscriptions by net revenue. Remaining subscriptions are aggregated into 'other'.        |