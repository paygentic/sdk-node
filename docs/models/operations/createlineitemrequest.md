# CreateLineItemRequest

## Example Usage

```typescript
import { CreateLineItemRequest } from "@paygentic/sdk/models/operations";

let value: CreateLineItemRequest = {
  createManualLineItemRequest: {
    displayName: "Gustave_Nitzsche",
    currency: "Moldovan Leu",
    quantity: 5763.12,
    unitPrice: 8965.89,
  },
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `idempotencyKey`                                                                                                | *string*                                                                                                        | :heavy_minus_sign:                                                                                              | Optional idempotency key. If provided, duplicate requests with the same key return the previously created item. |
| `createManualLineItemRequest`                                                                                   | [models.CreateManualLineItemRequest](../../models/createmanuallineitemrequest.md)                               | :heavy_check_mark:                                                                                              | N/A                                                                                                             |