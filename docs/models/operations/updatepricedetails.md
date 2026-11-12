# UpdatePriceDetails

## Example Usage

```typescript
import { UpdatePriceDetails } from "@paygentic/sdk/models/operations";

let value: UpdatePriceDetails = {};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `priceId`                                                           | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `fields`                                                            | *string*[]                                                          | :heavy_minus_sign:                                                  | N/A                                                                 |
| `subscriptionCount`                                                 | *number*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |
| `subscriptionProposalIds`                                           | *string*[]                                                          | :heavy_minus_sign:                                                  | Up to ten of the pending subscription proposals that name the price |
| `subscriptionProposalCount`                                         | *number*                                                            | :heavy_minus_sign:                                                  | How many pending subscription proposals name the price              |