# GroupedValue

## Example Usage

```typescript
import { GroupedValue } from "@paygentic/sdk/models";

let value: GroupedValue = {
  groupBy: {
    "key": "<value>",
    "key1": "<value>",
  },
  value: 8351.03,
};
```

## Fields

| Field                    | Type                     | Required                 | Description              |
| ------------------------ | ------------------------ | ------------------------ | ------------------------ |
| `groupBy`                | Record<string, *string*> | :heavy_check_mark:       | N/A                      |
| `value`                  | *number*                 | :heavy_check_mark:       | N/A                      |