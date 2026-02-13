# Tax

Tax reconciliation metadata (only present when plan has taxEnabled)

## Example Usage

```typescript
import { Tax } from "@paygentic/sdk/models";

let value: Tax = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `actualTax`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | Actual tax calculated (in atomic units)                                                       |
| `adjustmentApplied`                                                                           | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | Whether wallet adjustment was applied during tax reconciliation                               |
| `adjustmentNeeded`                                                                            | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | Whether wallet adjustment is needed (difference >= $0.01)                                     |
| `difference`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | Difference between actual and estimated (in atomic units)                                     |
| `estimatedTax`                                                                                | *string*                                                                                      | :heavy_minus_sign:                                                                            | Tax estimated from subscription rate (in atomic units)                                        |
| `reconciled`                                                                                  | *boolean*                                                                                     | :heavy_minus_sign:                                                                            | Whether reconciliation was performed                                                          |
| `reconciledAt`                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When reconciliation occurred                                                                  |