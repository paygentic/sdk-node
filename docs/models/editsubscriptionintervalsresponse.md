# EditSubscriptionIntervalsResponse

## Example Usage

```typescript
import { EditSubscriptionIntervalsResponse } from "@paygentic/sdk/models";

let value: EditSubscriptionIntervalsResponse = {
  intervals: [],
  unchanged: false,
  lineItems: {
    created: 445142,
    removed: 783812,
  },
  intervalChange: {
    id: "<id>",
    merchantId: "<id>",
    subscriptionId: "<id>",
    changeReason: "unspecified",
    description: "whether psst busily chunder regularly duh",
    metadata: {
      "key": 8016.64,
    },
    createdAt: new Date("2026-07-24T08:32:24.754Z"),
    intervals: [],
  },
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `intervals`                                                                                                  | [models.SubscriptionInterval](../models/subscriptioninterval.md)[]                                           | :heavy_check_mark:                                                                                           | The timeline's effective price intervals after applying the op set, ordered by start date.                   |
| `unchanged`                                                                                                  | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | True when the op set resolved to no change and nothing was written.                                          |
| `lineItems`                                                                                                  | [models.EditSubscriptionIntervalsResponseLineItems](../models/editsubscriptionintervalsresponselineitems.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `intervalChange`                                                                                             | [models.SubscriptionIntervalChange](../models/subscriptionintervalchange.md)                                 | :heavy_check_mark:                                                                                           | The record this edit wrote. Null when the edit changed nothing.                                              |