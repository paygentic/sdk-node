# SubscriptionCustomer

Customer details with merchant and consumer information. Only included when include=customer is specified in the list query.

## Example Usage

```typescript
import { SubscriptionCustomer } from "@paygentic/sdk/models";

let value: SubscriptionCustomer = {};
```

## Fields

| Field                                    | Type                                     | Required                                 | Description                              |
| ---------------------------------------- | ---------------------------------------- | ---------------------------------------- | ---------------------------------------- |
| `id`                                     | *string*                                 | :heavy_minus_sign:                       | Customer ID                              |
| `merchantId`                             | *string*                                 | :heavy_minus_sign:                       | Merchant organization ID                 |
| `merchant`                               | [models.Merchant](../models/merchant.md) | :heavy_minus_sign:                       | N/A                                      |
| `consumer`                               | [models.Consumer](../models/consumer.md) | :heavy_minus_sign:                       | N/A                                      |