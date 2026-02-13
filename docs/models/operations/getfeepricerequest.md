# GetFeePriceRequest

## Example Usage

```typescript
import { GetFeePriceRequest } from "@paygentic/sdk/models/operations";

let value: GetFeePriceRequest = {
  id: "<id>",
  subscriptionId: "<id>",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `id`                                       | *string*                                   | :heavy_check_mark:                         | The unique identifier of the fee.          |
| `subscriptionId`                           | *string*                                   | :heavy_check_mark:                         | The unique identifier of the subscription. |