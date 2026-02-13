# Failed

## Example Usage

```typescript
import { Failed } from "@paygentic/sdk/models";

let value: Failed = {
  error: "<value>",
  idempotencyKey: "<value>",
  index: 650433,
};
```

## Fields

| Field                                                   | Type                                                    | Required                                                | Description                                             |
| ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------- |
| `error`                                                 | *string*                                                | :heavy_check_mark:                                      | Error message describing why the event failed           |
| `idempotencyKey`                                        | *string*                                                | :heavy_check_mark:                                      | Idempotency key of the failed event for identification  |
| `index`                                                 | *number*                                                | :heavy_check_mark:                                      | Index of the failed event in the original request array |