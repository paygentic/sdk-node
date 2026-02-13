# ValidTaxAddress

Indicates whether the consumer address is valid for tax calculation when using Paygentic Tax. If valid=false, tax calculation will be skipped and internal invoice flow with default tax rate will be used.

## Example Usage

```typescript
import { ValidTaxAddress } from "@paygentic/sdk/models";

let value: ValidTaxAddress = {
  valid: false,
};
```

## Fields

| Field                                                                                                                                                                        | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `message`                                                                                                                                                                    | *string*                                                                                                                                                                     | :heavy_minus_sign:                                                                                                                                                           | Validation message if address is invalid. Sample values: 'Country is required for tax calculation', 'Invalid postal code format', 'State/province required for this country' |
| `valid`                                                                                                                                                                      | *boolean*                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                           | Whether the consumer address is valid for tax calculation when using Paygentic Tax                                                                                           |