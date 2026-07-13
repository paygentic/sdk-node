# InvoiceLineItemsResponse

## Example Usage

```typescript
import { InvoiceLineItemsResponse } from "@paygentic/sdk/models";

let value: InvoiceLineItemsResponse = {
  invoiceId: "<id>",
  lineItems: [
    {
      eventType: "fee",
      eventId: "<id>",
      eventSourceId: "<id>",
      billableMetricId: "<id>",
      invoiceDisplayName: "<value>",
      lineItemType: "refund",
      meterEventId: "<id>",
      metricDescription: "<value>",
      metricName: "<value>",
      metricUnit: "<value>",
      quantity: 2984.24,
      taxRate: 5627.65,
      totalAmount: "<value>",
      totalPrice: "<value>",
      totalTax: "<value>",
      unitPrice: "<value>",
    },
  ],
  totalCount: 697017,
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `invoiceId`                                              | *string*                                                 | :heavy_check_mark:                                       | The invoice ID                                           |
| `lineItems`                                              | [models.InvoiceLineItem](../models/invoicelineitem.md)[] | :heavy_check_mark:                                       | Array of line items for this page                        |
| `nextPageToken`                                          | *string*                                                 | :heavy_minus_sign:                                       | Token for fetching the next page, null if no more pages  |
| `totalCount`                                             | *number*                                                 | :heavy_check_mark:                                       | Total number of line items across all pages              |