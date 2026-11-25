# GetCreditPoolLedgerResponse

Pool ledger for the requested window. The shape depends on whether `granularity` was set: unset returns itemized `entries`, set returns rolled-up `buckets`.


## Supported Types

### `models.CreditPoolLedgerItemizedResponse`

```typescript
const value: models.CreditPoolLedgerItemizedResponse = {
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

### `models.CreditPoolLedgerBucketedResponse`

```typescript
const value: models.CreditPoolLedgerBucketedResponse = {
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

