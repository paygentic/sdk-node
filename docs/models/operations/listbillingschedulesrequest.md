# ListBillingSchedulesRequest

## Example Usage

```typescript
import { ListBillingSchedulesRequest } from "@paygentic/sdk/models/operations";

let value: ListBillingSchedulesRequest = {};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `orderId`                                        | *string*                                         | :heavy_minus_sign:                               | Filter by owning order (XOR with subscriptionId) |
| `subscriptionId`                                 | *string*                                         | :heavy_minus_sign:                               | Filter by owning subscription (XOR with orderId) |