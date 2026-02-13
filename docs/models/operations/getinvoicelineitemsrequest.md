# GetInvoiceLineItemsRequest

## Example Usage

```typescript
import { GetInvoiceLineItemsRequest } from "@paygentic/sdk/models/operations";

let value: GetInvoiceLineItemsRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | The invoice ID                                         |
| `limit`                                                | *number*                                               | :heavy_minus_sign:                                     | Maximum number of line items to return                 |
| `pageToken`                                            | *string*                                               | :heavy_minus_sign:                                     | Token for pagination to fetch the next page of results |