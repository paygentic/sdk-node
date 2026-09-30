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
};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `intervals`                                                                                                  | [models.SubscriptionInterval](../models/subscriptioninterval.md)[]                                           | :heavy_check_mark:                                                                                           | The timeline's effective price intervals after applying the op set, ordered by start date.                   |
| `unchanged`                                                                                                  | *boolean*                                                                                                    | :heavy_check_mark:                                                                                           | True when the op set resolved to no change and nothing was written.                                          |
| `lineItems`                                                                                                  | [models.EditSubscriptionIntervalsResponseLineItems](../models/editsubscriptionintervalsresponselineitems.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |