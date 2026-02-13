# CustomerOrganization

## Example Usage

```typescript
import { CustomerOrganization } from "@paygentic/sdk/models";

let value: CustomerOrganization = {
  id: "<id>",
  name: "<value>",
};
```

## Fields

| Field                                  | Type                                   | Required                               | Description                            |
| -------------------------------------- | -------------------------------------- | -------------------------------------- | -------------------------------------- |
| `id`                                   | *string*                               | :heavy_check_mark:                     | N/A                                    |
| `address`                              | [models.Address](../models/address.md) | :heavy_minus_sign:                     | N/A                                    |
| `billingEmail`                         | *string*                               | :heavy_minus_sign:                     | N/A                                    |
| `name`                                 | *string*                               | :heavy_check_mark:                     | N/A                                    |
| `phone`                                | *string*                               | :heavy_minus_sign:                     | N/A                                    |