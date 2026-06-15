# ListSalesforceAccountsRequest

## Example Usage

```typescript
import { ListSalesforceAccountsRequest } from "@paygentic/sdk/models/operations";

let value: ListSalesforceAccountsRequest = {
  merchantId: "<id>",
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `merchantId`                                 | *string*                                     | :heavy_check_mark:                           | Merchant whose Salesforce connection to use. |
| `q`                                          | *string*                                     | :heavy_minus_sign:                           | Optional name filter (LIKE match).           |
| `limit`                                      | *number*                                     | :heavy_minus_sign:                           | N/A                                          |
| `offset`                                     | *number*                                     | :heavy_minus_sign:                           | N/A                                          |