# PaymentSummary

## Example Usage

```typescript
import { PaymentSummary } from "@paygentic/sdk/models";

let value: PaymentSummary = {
  completedCount: 24334,
  completedAmount: "<value>",
  pendingCount: 794242,
  pendingAmount: "<value>",
  expiredCount: 411756,
  expiredAmount: "<value>",
};
```

## Fields

| Field                                              | Type                                               | Required                                           | Description                                        |
| -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- | -------------------------------------------------- |
| `completedCount`                                   | *number*                                           | :heavy_check_mark:                                 | Number of completed payment links in the period    |
| `completedAmount`                                  | *string*                                           | :heavy_check_mark:                                 | Total amount of completed payment links in dollars |
| `pendingCount`                                     | *number*                                           | :heavy_check_mark:                                 | Number of pending payment links in the period      |
| `pendingAmount`                                    | *string*                                           | :heavy_check_mark:                                 | Total amount of pending payment links in dollars   |
| `expiredCount`                                     | *number*                                           | :heavy_check_mark:                                 | Number of expired payment links in the period      |
| `expiredAmount`                                    | *string*                                           | :heavy_check_mark:                                 | Total amount of expired payment links in dollars   |