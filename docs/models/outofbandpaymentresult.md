# OutOfBandPaymentResult

## Example Usage

```typescript
import { OutOfBandPaymentResult } from "@paygentic/sdk/models";

let value: OutOfBandPaymentResult = {
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

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `method`                                            | *"out_of_band"*                                     | :heavy_check_mark:                                  | Discriminator: an out-of-band payment was recorded. |
| `invoice`                                           | [models.Invoice](../models/invoice.md)              | :heavy_check_mark:                                  | N/A                                                 |