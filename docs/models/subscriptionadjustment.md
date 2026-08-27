# SubscriptionAdjustment

## Example Usage

```typescript
import { SubscriptionAdjustment } from "@paygentic/sdk/models";

let value: SubscriptionAdjustment = {
  object: "subscriptionAdjustment",
  id: "<id>",
  subscriptionId: "<id>",
  type: "percentageDiscount",
  percentageDiscount: "<value>",
  effectiveFrom: new Date("2024-11-09T13:46:27.367Z"),
  effectiveTo: new Date("2025-07-13T07:52:43.445Z"),
  description: "past unknown obsess till extremely including",
  createdAt: new Date("2025-01-04T01:20:55.026Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.SubscriptionAdjustmentObject](../models/subscriptionadjustmentobject.md)              | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | The adjustment ID                                                                             |
| `subscriptionId`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a subscription                                                          |
| `type`                                                                                        | [models.SubscriptionAdjustmentType](../models/subscriptionadjustmenttype.md)                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `percentageDiscount`                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | The discount rate as a decimal fraction between 0 and 1. "0.35" means 35 percent.             |
| `effectiveFrom`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | The first instant the discount applies. Inclusive.                                            |
| `effectiveTo`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | The instant the discount stops applying. Exclusive. Null means the discount never stops.      |
| `description`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | The deal's own name, shown on each discount line of the invoice.                              |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |