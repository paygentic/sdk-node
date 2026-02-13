# RequestBody1

## Example Usage

```typescript
import { RequestBody1 } from "@paygentic/sdk/models/operations";

let value: RequestBody1 = {
  currentTime: new Date("2024-01-02T01:10:36.384Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `currentTime`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | New absolute time for the test clock (must be forward in time)                                |