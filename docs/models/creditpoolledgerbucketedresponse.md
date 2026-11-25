# CreditPoolLedgerBucketedResponse

## Example Usage

```typescript
import { CreditPoolLedgerBucketedResponse } from "@paygentic/sdk/models";

let value: CreditPoolLedgerBucketedResponse = {
  startingBalance: 2859.89,
  endingBalance: 3749.95,
  buckets: [
    {
      period: {
        from: new Date("2025-10-23T14:35:18.486Z"),
        to: new Date("2026-05-13T03:04:33.938Z"),
      },
      startingBalance: 3882.43,
      endingBalance: 588.59,
      incremented: 2472.97,
      decremented: 5961.65,
      voided: 9673.52,
      expired: 9958.75,
      entryCount: 741481,
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                                                                      | Type                                                                                                                       | Required                                                                                                                   | Description                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `startingBalance`                                                                                                          | *number*                                                                                                                   | :heavy_check_mark:                                                                                                         | Pool's total balance at the requested window's `from`.                                                                     |
| `endingBalance`                                                                                                            | *number*                                                                                                                   | :heavy_check_mark:                                                                                                         | Pool's total balance at the requested window's `to`.                                                                       |
| `buckets`                                                                                                                  | [models.CreditPoolLedgerBucket](../models/creditpoolledgerbucket.md)[]                                                     | :heavy_check_mark:                                                                                                         | Calendar-aligned buckets within the requested window, ordered oldest first. A calendar period with no activity is omitted. |
| `pagination`                                                                                                               | [models.OffsetPagination](../models/offsetpagination.md)                                                                   | :heavy_check_mark:                                                                                                         | Offset-based pagination response.                                                                                          |