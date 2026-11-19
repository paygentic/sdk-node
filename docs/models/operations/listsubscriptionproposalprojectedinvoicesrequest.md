# ListSubscriptionProposalProjectedInvoicesRequest

## Example Usage

```typescript
import { ListSubscriptionProposalProjectedInvoicesRequest } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionProposalProjectedInvoicesRequest = {
  id: "<id>",
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `id`                                      | *string*                                  | :heavy_check_mark:                        | The subscription proposal ID              |
| `limit`                                   | *number*                                  | :heavy_minus_sign:                        | Maximum number of invoices to return      |
| `offset`                                  | *number*                                  | :heavy_minus_sign:                        | Number of invoices to skip for pagination |