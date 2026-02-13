# ListSourceEventsRequest

## Example Usage

```typescript
import { ListSourceEventsRequest } from "@paygentic/sdk/models/operations";

let value: ListSourceEventsRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `id`                                                                                   | *string*                                                                               | :heavy_check_mark:                                                                     | N/A                                                                                    |
| `customerId`                                                                           | *string*                                                                               | :heavy_minus_sign:                                                                     | Filter events by customer ID                                                           |
| `limit`                                                                                | *number*                                                                               | :heavy_minus_sign:                                                                     | N/A                                                                                    |
| `offset`                                                                               | *number*                                                                               | :heavy_minus_sign:                                                                     | N/A                                                                                    |
| `status`                                                                               | [operations.ListSourceEventsStatus](../../models/operations/listsourceeventsstatus.md) | :heavy_minus_sign:                                                                     | Filter events by status                                                                |
| `subscriptionId`                                                                       | *string*                                                                               | :heavy_minus_sign:                                                                     | Filter events by subscription ID                                                       |