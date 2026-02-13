# GetActiveEntitlementsRequest

## Example Usage

```typescript
import { GetActiveEntitlementsRequest } from "@paygentic/sdk/models/operations";

let value: GetActiveEntitlementsRequest = {
  customerId: "<id>",
};
```

## Fields

| Field                                               | Type                                                | Required                                            | Description                                         |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| `customerId`                                        | *string*                                            | :heavy_check_mark:                                  | The customer ID to get active entitlements for.     |
| `productId`                                         | *string*                                            | :heavy_minus_sign:                                  | The product ID to get active entitlements for.      |
| `subscriptionId`                                    | *string*                                            | :heavy_minus_sign:                                  | The subscription ID to get active entitlements for. |