# DeletePriceConflictError

Price cannot be deleted because a live plan still references it

## Example Usage

```typescript
import { DeletePriceConflictError } from "@paygentic/sdk/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `error`                                                                        | *string*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |
| `message`                                                                      | *string*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |
| `details`                                                                      | [operations.DeletePriceDetails](../../models/operations/deletepricedetails.md) | :heavy_minus_sign:                                                             | N/A                                                                            |