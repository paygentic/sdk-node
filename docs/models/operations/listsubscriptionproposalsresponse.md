# ListSubscriptionProposalsResponse

Subscription proposals

## Example Usage

```typescript
import { ListSubscriptionProposalsResponse } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionProposalsResponse = {
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `data`                                                                | [models.SubscriptionProposal](../../models/subscriptionproposal.md)[] | :heavy_check_mark:                                                    | N/A                                                                   |
| `pagination`                                                          | [models.OffsetPagination](../../models/offsetpagination.md)           | :heavy_check_mark:                                                    | Offset-based pagination response.                                     |