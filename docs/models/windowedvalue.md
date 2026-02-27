# WindowedValue

## Example Usage

```typescript
import { WindowedValue } from "@paygentic/sdk/models";

let value: WindowedValue = {
  windowStart: new Date("2026-05-03T00:23:39.112Z"),
  windowEnd: new Date("2024-11-15T19:44:14.930Z"),
  value: 2754.03,
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `windowStart`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `windowEnd`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `value`                                                                                       | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |