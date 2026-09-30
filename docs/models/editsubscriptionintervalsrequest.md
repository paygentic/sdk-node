# EditSubscriptionIntervalsRequest

An add/edit/remove op set to apply to the subscription's price timeline. At least one operation is required.

## Example Usage

```typescript
import { EditSubscriptionIntervalsRequest } from "@paygentic/sdk/models";

let value: EditSubscriptionIntervalsRequest = {};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `add`                                                                              | [models.SubscriptionIntervalAddOp](../models/subscriptionintervaladdop.md)[]       | :heavy_minus_sign:                                                                 | New override segments to add.                                                      |
| `edit`                                                                             | [models.SubscriptionIntervalEditOp](../models/subscriptionintervaleditop.md)[]     | :heavy_minus_sign:                                                                 | Changes to existing intervals.                                                     |
| `remove`                                                                           | [models.SubscriptionIntervalRemoveOp](../models/subscriptionintervalremoveop.md)[] | :heavy_minus_sign:                                                                 | Intervals to remove outright.                                                      |