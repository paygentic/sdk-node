# ReplaceScheduleIntervalsRequest

## Example Usage

```typescript
import { ReplaceScheduleIntervalsRequest } from "@paygentic/sdk/models";

let value: ReplaceScheduleIntervalsRequest = {
  intervals: [
    {
      baseQuantity: "<value>",
      billingCadence: "<value>",
      startDate: new Date("2026-11-14T12:43:56.489Z"),
      endDate: new Date("2024-08-07T19:34:20.603Z"),
    },
  ],
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `intervals`                                                                      | [models.Interval](../models/interval.md)[]                                       | :heavy_check_mark:                                                               | N/A                                                                              |
| `orderLineItemId`                                                                | *string*                                                                         | :heavy_minus_sign:                                                               | When set, scope the wipe to this line's intervals only (per-line cell-edit path) |