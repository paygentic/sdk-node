# UsagePeriod

## Example Usage

```typescript
import { UsagePeriod } from "@paygentic/sdk/models";

let value: UsagePeriod = {
  interval: "<value>",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `interval`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ISO 8601 duration for the usage period, e.g. P1D, P1W, P1M, P1Y.                              |
| `anchor`                                                                                      | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Optional anchor date-time for period alignment.                                               |