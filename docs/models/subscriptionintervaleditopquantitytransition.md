# SubscriptionIntervalEditOpQuantityTransition

## Example Usage

```typescript
import { SubscriptionIntervalEditOpQuantityTransition } from "@paygentic/sdk/models";

let value: SubscriptionIntervalEditOpQuantityTransition = {
  effectiveDate: new Date("2026-06-16T06:39:47.790Z"),
  quantity: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `effectiveDate`                                                                               | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `quantity`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | Non-negative decimal string.                                                                  |