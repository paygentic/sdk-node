# ReplaceScheduleIntervalsRequest

## Example Usage

```typescript
import { ReplaceScheduleIntervalsRequest } from "@paygentic/sdk/models/operations";

let value: ReplaceScheduleIntervalsRequest = {
  id: "<id>",
  replaceScheduleIntervalsRequest: {
    intervals: [
      {
        baseQuantity: "<value>",
        billingCadence: "<value>",
        startDate: new Date("2026-11-14T12:43:56.489Z"),
        endDate: new Date("2024-08-07T19:34:20.603Z"),
      },
    ],
  },
};
```

## Fields

| Field                                                                                     | Type                                                                                      | Required                                                                                  | Description                                                                               |
| ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `id`                                                                                      | *string*                                                                                  | :heavy_check_mark:                                                                        | N/A                                                                                       |
| `replaceScheduleIntervalsRequest`                                                         | [models.ReplaceScheduleIntervalsRequest](../../models/replacescheduleintervalsrequest.md) | :heavy_check_mark:                                                                        | N/A                                                                                       |