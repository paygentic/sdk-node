# Address

Address is required for tax calculation. Must include: country (ISO 3166-1 alpha-2) and zipCode. The state/region field is required and validated for US/CA addresses only (custom validation in API logic). Postal code format is not validated but will be normalized.

## Example Usage

```typescript
import { Address } from "@paygentic/sdk/models/operations";

let value: Address = {
  country: "Aruba",
  zipCode: "84082",
};
```

## Fields

| Field                             | Type                              | Required                          | Description                       |
| --------------------------------- | --------------------------------- | --------------------------------- | --------------------------------- |
| `line1`                           | *string*                          | :heavy_minus_sign:                | N/A                               |
| `line2`                           | *string*                          | :heavy_minus_sign:                | N/A                               |
| `city`                            | *string*                          | :heavy_minus_sign:                | N/A                               |
| `state`                           | *string*                          | :heavy_minus_sign:                | N/A                               |
| `country`                         | *string*                          | :heavy_check_mark:                | 2 character ISO 3166 country code |
| `zipCode`                         | *string*                          | :heavy_check_mark:                | N/A                               |