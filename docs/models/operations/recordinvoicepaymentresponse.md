# RecordInvoicePaymentResponse

The invoice is settled, or a new payment link exists. The `method` field identifies the shape: `out_of_band` returns the `PAID` invoice; `hosted_link` returns the provider and the new payment link.


## Supported Types

### `models.OutOfBandPaymentResult`

```typescript
const value: models.OutOfBandPaymentResult = {
  method: "out_of_band",
  invoice: {
    id: "<id>",
    object: "invoice",
    autoApprove: false,
    billingAnchor: new Date("2024-07-10T23:17:47.301Z"),
    billingCadence: "<value>",
    createdAt: new Date("2026-07-12T01:26:36.944Z"),
    currency: "Mauritius Rupee",
    gracePeriodEnd: new Date("2026-02-14T03:30:30.008Z"),
    grandTotal: "<value>",
    itemCount: 275482,
    merchantId: "<id>",
    paidAmount: "<value>",
    periodEnd: new Date("2026-01-04T04:43:04.003Z"),
    periodStart: new Date("2024-09-03T19:53:59.571Z"),
    sequenceNumber: 792149,
    status: "ISSUED",
    subscriptionId: "<id>",
    customerId: "<id>",
    subtotal: "<value>",
    totalTax: "<value>",
    unpaidAmount: "<value>",
    updatedAt: new Date("2024-10-15T07:06:59.916Z"),
  },
};
```

### `models.HostedLinkPaymentResult`

```typescript
const value: models.HostedLinkPaymentResult = {
  method: "hosted_link",
  provider: "airwallex",
  paymentSessionId: "<id>",
  paymentUrl: "https://rectangular-scale.net/",
  invoice: {
    id: "<id>",
    object: "invoice",
    autoApprove: false,
    billingAnchor: new Date("2024-07-10T23:17:47.301Z"),
    billingCadence: "<value>",
    createdAt: new Date("2026-07-12T01:26:36.944Z"),
    currency: "Mauritius Rupee",
    gracePeriodEnd: new Date("2026-02-14T03:30:30.008Z"),
    grandTotal: "<value>",
    itemCount: 275482,
    merchantId: "<id>",
    paidAmount: "<value>",
    periodEnd: new Date("2026-01-04T04:43:04.003Z"),
    periodStart: new Date("2024-09-03T19:53:59.571Z"),
    sequenceNumber: 792149,
    status: "ISSUED",
    subscriptionId: "<id>",
    customerId: "<id>",
    subtotal: "<value>",
    totalTax: "<value>",
    unpaidAmount: "<value>",
    updatedAt: new Date("2024-10-15T07:06:59.916Z"),
  },
};
```

