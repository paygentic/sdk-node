# MeterEvent

## Example Usage

```typescript
import { MeterEvent } from "@paygentic/sdk/models";

let value: MeterEvent = {
  id: "<id>",
  type: "<value>",
  source: "<value>",
  subject: "<value>",
  time: new Date("2025-08-12T00:53:29.185Z"),
  idempotencyKey: "<value>",
  data: {
    "key": "<value>",
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique event identifier                                                                       |
| `object`                                                                                      | [models.MeterEventObject](../models/metereventobject.md)                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `type`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | CloudEvents event type (matches the meter's eventType)                                        |
| `source`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | CloudEvents source that published the event                                                   |
| `subject`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | Subject of the event — typically the customer ID                                              |
| `time`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Time the event occurred                                                                       |
| `idempotencyKey`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Caller-supplied idempotency key                                                               |
| `data`                                                                                        | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | Event payload                                                                                 |