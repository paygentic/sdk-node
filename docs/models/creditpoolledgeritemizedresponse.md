# CreditPoolLedgerItemizedResponse

## Example Usage

```typescript
import { CreditPoolLedgerItemizedResponse } from "@paygentic/sdk/models";

let value: CreditPoolLedgerItemizedResponse = {
  startingBalance: 3083.76,
  endingBalance: 714.53,
  entries: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `startingBalance`                                                    | *number*                                                             | :heavy_check_mark:                                                   | Pool's total balance at the requested window's `from`.               |
| `endingBalance`                                                      | *number*                                                             | :heavy_check_mark:                                                   | Pool's total balance at the requested window's `to`.                 |
| `entries`                                                            | [models.CreditPoolLedgerEntry](../models/creditpoolledgerentry.md)[] | :heavy_check_mark:                                                   | Ledger entries within the requested window, ordered oldest first.    |
| `pagination`                                                         | [models.OffsetPagination](../models/offsetpagination.md)             | :heavy_check_mark:                                                   | Offset-based pagination response.                                    |