# Stale

Present only when the database can't be reached, or the list takes more than a second to compute. The response is then the last result for this same request in the past hour, computed at `computedAt`.

## Example Usage

```typescript
import { Stale } from "@paygentic/sdk/models/operations";

let value: Stale = {
  computedAt: new Date("2024-03-11T18:16:45.029Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `computedAt`                                                                                  | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When this result was computed.                                                                |