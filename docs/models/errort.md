# ErrorT

## Example Usage

```typescript
import { ErrorT } from "@paygentic/sdk/models";

let value: ErrorT = {
  field: "<value>",
  message: "<value>",
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `field`                                 | *string*                                | :heavy_check_mark:                      | The field that failed validation        |
| `message`                               | *string*                                | :heavy_check_mark:                      | Validation error message for this field |
| `code`                                  | *string*                                | :heavy_minus_sign:                      | Validation error code                   |