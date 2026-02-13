# ValidationError

## Example Usage

```typescript
import { ValidationError } from "@paygentic/sdk/models/errors";

// No examples available for this model
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `error`                                       | [models.ErrorEnum](../../models/errorenum.md) | :heavy_minus_sign:                            | Error type indicating validation failure      |
| `message`                                     | *string*                                      | :heavy_check_mark:                            | Human-readable error message                  |
| `errors`                                      | [models.ErrorT](../../models/errort.md)[]     | :heavy_check_mark:                            | Array of field-specific validation errors     |