# RevenueStats

## Example Usage

```typescript
import { RevenueStats } from "@paygentic/sdk/models";

let value: RevenueStats = {};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `usageRevenue`                                  | *string*                                        | :heavy_minus_sign:                              | Revenue from usage charges in dollars           |
| `feeRevenue`                                    | *string*                                        | :heavy_minus_sign:                              | Revenue from fee charges in dollars             |
| `refundAmount`                                  | *string*                                        | :heavy_minus_sign:                              | Total refund amount in dollars                  |
| `netRevenue`                                    | *string*                                        | :heavy_minus_sign:                              | Net revenue in dollars (usage + fees - refunds) |
| `usageCount`                                    | *number*                                        | :heavy_minus_sign:                              | Number of usage charge events                   |
| `feeCount`                                      | *number*                                        | :heavy_minus_sign:                              | Number of fee charge events                     |
| `usageRefundCount`                              | *number*                                        | :heavy_minus_sign:                              | Number of usage refund events                   |
| `feeRefundCount`                                | *number*                                        | :heavy_minus_sign:                              | Number of fee refund events                     |