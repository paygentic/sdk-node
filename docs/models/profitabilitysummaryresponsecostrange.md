# ProfitabilitySummaryResponseCostRange

Where the caller's cost data actually lies in time. Present only when the selected range returned no cost. An object carries the bounds of the real cost events; null means the caller has no cost event at any time; an absent field means the extent was not resolved, because the result was not empty, because the lookup failed, or because the metering service does not serve the bounds method. An absent field must never be read as an absence.

## Example Usage

```typescript
import { ProfitabilitySummaryResponseCostRange } from "@paygentic/sdk/models";

let value: ProfitabilitySummaryResponseCostRange = {
  from: new Date("2025-10-11T20:56:12.988Z"),
  to: new Date("2026-09-04T08:06:26.256Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Earliest cost event instant.                                                                  |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Latest cost event instant.                                                                    |