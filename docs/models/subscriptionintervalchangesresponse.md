# SubscriptionIntervalChangesResponse

## Example Usage

```typescript
import { SubscriptionIntervalChangesResponse } from "@paygentic/sdk/models";

let value: SubscriptionIntervalChangesResponse = {
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `data`                                                                         | [models.SubscriptionIntervalChange](../models/subscriptionintervalchange.md)[] | :heavy_check_mark:                                                             | N/A                                                                            |
| `pagination`                                                                   | [models.OffsetPagination](../models/offsetpagination.md)                       | :heavy_check_mark:                                                             | Offset-based pagination response.                                              |