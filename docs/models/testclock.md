# TestClock

## Example Usage

```typescript
import { TestClock } from "@paygentic/sdk/models";

let value: TestClock = {
  id: "<id>",
  createdAt: new Date("2025-02-06T00:40:16.566Z"),
  currentTime: new Date("2025-10-09T17:39:55.805Z"),
  merchantId: "<id>",
  updatedAt: new Date("2024-05-25T09:15:21.310Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for the test clock                                                          |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the test clock was created                                                               |
| `currentTime`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | The simulated current time of the test clock                                                  |
| `deletedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | When the test clock was deleted (if applicable)                                               |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | Description of the test clock's purpose                                                       |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | The merchant organization that owns this test clock                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | Name of the test clock                                                                        |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the test clock was last updated                                                          |