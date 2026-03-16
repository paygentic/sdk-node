# PaymentUnion

Payment session details when upfront payment is required, or confirmation of a zero-amount paid invoice


## Supported Types

### `models.PaymentPending`

```typescript
const value: models.PaymentPending = {
  amount: "418.24",
  breakdown: {
    upfrontCharges: "<value>",
    walletCharge: "<value>",
  },
  checkoutUrl: "https://juvenile-napkin.biz",
  paymentSessionId: "<id>",
  status: "pending",
};
```

### `models.PaymentPaid`

```typescript
const value: models.PaymentPaid = {
  invoiceId: "<id>",
  amount: "726.92",
  status: "paid",
};
```

