# ActiveEntitlement

## Example Usage

```typescript
import { ActiveEntitlement } from "@paygentic/sdk/models";

let value: ActiveEntitlement = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_minus_sign:                                                                            | Unique identifier for an entitlement                                                          |
| `object`                                                                                      | [models.ActiveEntitlementObject](../models/activeentitlementobject.md)                        | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `billableMetrics`                                                                             | *string*[]                                                                                    | :heavy_minus_sign:                                                                            | List of billable metrics that this entitlement covers.                                        |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_minus_sign:                                                                            | Unique identifier for a customer                                                              |
| `planId`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | Unique identifier for a plan                                                                  |
| `productId`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | Unique identifier for a product                                                               |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_minus_sign:                                                                            | Unique identifier for a subscription                                                          |
| `verifiedAt`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Timestamp when the entitlement was checked.                                                   |