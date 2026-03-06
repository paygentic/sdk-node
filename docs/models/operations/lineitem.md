# LineItem

## Example Usage

```typescript
import { LineItem } from "@paygentic/sdk/models/operations";

let value: LineItem = {
  description: "minor painfully thorny boohoo assail",
  amount: "860.98",
};
```

## Fields

| Field                                             | Type                                              | Required                                          | Description                                       |
| ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------- |
| `description`                                     | *string*                                          | :heavy_check_mark:                                | Line item description.                            |
| `amount`                                          | *string*                                          | :heavy_check_mark:                                | Line item amount in decimal format (e.g. '5.00'). |
| `quantity`                                        | *number*                                          | :heavy_minus_sign:                                | Quantity of this line item. Defaults to 1.        |