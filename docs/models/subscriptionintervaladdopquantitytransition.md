# SubscriptionIntervalAddOpQuantityTransition

## Example Usage

```typescript
import { SubscriptionIntervalAddOpQuantityTransition } from "@paygentic/sdk/models";

let value: SubscriptionIntervalAddOpQuantityTransition = {
  effectiveDate: new Date("2025-07-31T15:01:40.738Z"),
  quantity: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `effectiveDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `quantity`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Non-negative decimal string.                                                                  |