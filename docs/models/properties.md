# Properties

## Example Usage

```typescript
import { Properties } from "@paygentic/sdk/models";

let value: Properties = {
  unitPrice: "<value>",
};
```

## Fields

| Field                                                                                                                   | Type                                                                                                                    | Required                                                                                                                | Description                                                                                                             |
| ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| `unitPrice`                                                                                                             | *string*                                                                                                                | :heavy_check_mark:                                                                                                      | The unit price in dollars (e.g., '10.00'). Per unit. Total per period = quantity × unitPrice; see the `quantity` field. |