# ListSalesforceAccountsResponse

List of Salesforce accounts

## Example Usage

```typescript
import { ListSalesforceAccountsResponse } from "@paygentic/sdk/models/operations";

let value: ListSalesforceAccountsResponse = {
  data: [
    {
      "key": "<value>",
    },
    {
      "key": "<value>",
      "key1": "<value>",
    },
  ],
  totalSize: 890096,
  done: true,
};
```

## Fields

| Field                   | Type                    | Required                | Description             |
| ----------------------- | ----------------------- | ----------------------- | ----------------------- |
| `data`                  | Record<string, *any*>[] | :heavy_check_mark:      | N/A                     |
| `totalSize`             | *number*                | :heavy_check_mark:      | N/A                     |
| `done`                  | *boolean*               | :heavy_check_mark:      | N/A                     |