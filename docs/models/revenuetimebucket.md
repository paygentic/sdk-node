# RevenueTimeBucket

## Example Usage

```typescript
import { RevenueTimeBucket } from "@paygentic/sdk/models";

let value: RevenueTimeBucket = {
  timestamp: new Date("2025-10-16T07:29:55.675Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `timestamp`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Start time of this bucket                                                                     |
| `subscriptionStats`                                                                           | Record<string, [models.RevenueStats](../models/revenuestats.md)>                              | :heavy_minus_sign:                                                                            | Revenue stats per subscription ID. May include 'other' for subscriptions outside top N.       |
| `totalStats`                                                                                  | [models.RevenueStats](../models/revenuestats.md)                                              | :heavy_minus_sign:                                                                            | N/A                                                                                           |