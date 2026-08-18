# PlanVersion

A single plan version, including its price slots. Extends the list summary with the version's prices.

## Example Usage

```typescript
import { PlanVersion } from "@paygentic/sdk/models";

let value: PlanVersion = {
  id: "<id>",
  object: "plan_version",
  versionNumber: 979541,
  status: "published",
  isDefault: false,
  subscriptionCount: 205549,
  updatedAt: new Date("2026-04-19T17:11:50.389Z"),
  prices: [],
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                         | *string*                                                                                                     | :heavy_check_mark:                                                                                           | Unique identifier for a plan version                                                                         |
| `object`                                                                                                     | [models.PlanVersionObject](../models/planversionobject.md)                                                   | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `versionNumber`                                                                                              | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Monotonic version number within the plan, starting at 1.                                                     |
| `status`                                                                                                     | [models.PlanVersionStatus](../models/planversionstatus.md)                                                   | :heavy_check_mark:                                                                                           | Lifecycle status of the version.                                                                             |
| `publishedAt`                                                                                                | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                | :heavy_minus_sign:                                                                                           | When this version was published.                                                                             |
| `isDefault`                                                                                                  | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | Whether this version is the plan's current default (live) version.                                           |
| `subscriptionCount`                                                                                          | *number*                                                                                                     | :heavy_check_mark:                                                                                           | Number of committed-status subscriptions pinned to this version at creation time. Not a live-billing cohort. |
| `basedOnVersionId`                                                                                           | *string*                                                                                                     | :heavy_minus_sign:                                                                                           | Unique identifier for a plan version                                                                         |
| `updatedAt`                                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                | :heavy_check_mark:                                                                                           | When this version was last modified.                                                                         |
| `prices`                                                                                                     | [models.PlanVersionPriceSlot](../models/planversionpriceslot.md)[]                                           | :heavy_check_mark:                                                                                           | The price slots that make up this version.                                                                   |