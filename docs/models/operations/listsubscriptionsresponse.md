# ListSubscriptionsResponse

List of subscriptions

## Example Usage

```typescript
import { ListSubscriptionsResponse } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionsResponse = {};
```

## Fields

| Field                                                       | Type                                                        | Required                                                    | Description                                                 |
| ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- | ----------------------------------------------------------- |
| `data`                                                      | [models.Subscription](../../models/subscription.md)[]       | :heavy_minus_sign:                                          | N/A                                                         |
| `pagination`                                                | [models.OffsetPagination](../../models/offsetpagination.md) | :heavy_minus_sign:                                          | Offset-based pagination response.                           |