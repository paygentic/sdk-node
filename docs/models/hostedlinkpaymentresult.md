# HostedLinkPaymentResult

## Example Usage

```typescript
import { HostedLinkPaymentResult } from "@paygentic/sdk/models";

let value: HostedLinkPaymentResult = {
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

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `method`                                                             | *"hosted_link"*                                                      | :heavy_check_mark:                                                   | Discriminator: a hosted payment link was minted/regenerated.         |
| `provider`                                                           | [models.InvoicePaymentProvider](../models/invoicepaymentprovider.md) | :heavy_check_mark:                                                   | The payment provider that a hosted payment link routes to.           |
| `paymentSessionId`                                                   | *string*                                                             | :heavy_check_mark:                                                   | The newly created payment session ID.                                |
| `paymentUrl`                                                         | *string*                                                             | :heavy_check_mark:                                                   | The customer-facing payment link for the new session.                |
| `invoice`                                                            | [models.Invoice](../models/invoice.md)                               | :heavy_check_mark:                                                   | N/A                                                                  |