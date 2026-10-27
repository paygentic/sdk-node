# Period

The read window, as requested: the report counts from <= t < to. Unlike `costRange`, `to` is not an instant the report covers, so a chart axis ends before it.

## Example Usage

```typescript
import { Period } from "@paygentic/sdk/models";

let value: Period = {
  from: new Date("2025-04-17T01:12:19.083Z"),
  to: new Date("2024-06-04T12:48:35.305Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Start of the read window, included.                                                           |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | End of the read window, excluded.                                                             |