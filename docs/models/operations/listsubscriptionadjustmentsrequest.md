# ListSubscriptionAdjustmentsRequest

## Example Usage

```typescript
import { ListSubscriptionAdjustmentsRequest } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionAdjustmentsRequest = {
  id: "<id>",
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `id`                            | *string*                        | :heavy_check_mark:              | The subscription ID             |
| `limit`                         | *string*                        | :heavy_minus_sign:              | Number of adjustments to return |
| `offset`                        | *string*                        | :heavy_minus_sign:              | Number of adjustments to skip   |