# ListSubscriptionIntervalChangesRequest

## Example Usage

```typescript
import { ListSubscriptionIntervalChangesRequest } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionIntervalChangesRequest = {
  id: "<id>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `id`                                 | *string*                             | :heavy_check_mark:                   | The subscription ID                  |
| `limit`                              | *string*                             | :heavy_minus_sign:                   | Number of interval changes to return |
| `offset`                             | *string*                             | :heavy_minus_sign:                   | Number of interval changes to skip   |