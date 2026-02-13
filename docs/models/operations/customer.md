# Customer

Fields to create a new customer and consumer. Will use an existing consumer if one exists with the same email address. Required if `customerId` is not provided. Address with complete tax information (country, state, zipCode) is required for tax calculation when using Paygentic Tax.

## Example Usage

```typescript
import { Customer } from "@paygentic/sdk/models/operations";

let value: Customer = {
  name: "<value>",
  email: "Abraham90@hotmail.com",
  address: {
    country: "Serbia",
    zipCode: "99348-7775",
  },
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `name`                                                                                           | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `email`                                                                                          | *string*                                                                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `phone`                                                                                          | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `address`                                                                                        | [operations.Address](../../models/operations/address.md)                                         | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `taxRates`                                                                                       | Record<string, *number*>                                                                         | :heavy_minus_sign:                                                                               | An object mapping plan IDs, metric IDs, or 'default' to a tax rate percentage (e.g., 13 for 13%) |