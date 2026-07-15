# AdvanceTestClockRequestBody1

## Example Usage

```typescript
import { AdvanceTestClockRequestBody1 } from "@paygentic/sdk/models/operations";

let value: AdvanceTestClockRequestBody1 = {
  currentTime: new Date("2025-07-19T03:15:59.942Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `currentTime`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | New absolute time for the test clock (must be forward in time)                                |