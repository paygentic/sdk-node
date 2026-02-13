# ListCustomersRequest

## Example Usage

```typescript
import { ListCustomersRequest } from "@paygentic/sdk/models/operations";

let value: ListCustomersRequest = {
  organizationId: "<id>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `limit`                                                | *number*                                               | :heavy_minus_sign:                                     | Number of customers to return                          |
| `offset`                                               | *number*                                               | :heavy_minus_sign:                                     | Number of customers to skip                            |
| `organizationId`                                       | *string*                                               | :heavy_check_mark:                                     | ID of the merchant organization to filter customers by |