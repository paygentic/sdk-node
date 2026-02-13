# UpdateUserRequestBody

## Example Usage

```typescript
import { UpdateUserRequestBody } from "@paygentic/sdk/models/operations";

let value: UpdateUserRequestBody = {};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `address`                                                              | [models.Address](../../models/address.md)                              | :heavy_minus_sign:                                                     | N/A                                                                    |
| `dateOfBirth`                                                          | [RFCDate](../../types/rfcdate.md)                                      | :heavy_minus_sign:                                                     | The date of birth of the user.                                         |
| `firstName`                                                            | *string*                                                               | :heavy_minus_sign:                                                     | The first name of the user.                                            |
| `lastName`                                                             | *string*                                                               | :heavy_minus_sign:                                                     | The last name of the user.                                             |
| `phone`                                                                | *string*                                                               | :heavy_minus_sign:                                                     | The phone number of the user.                                          |
| `type`                                                                 | [operations.UpdateUserType](../../models/operations/updateusertype.md) | :heavy_minus_sign:                                                     | Type of entity the user represents.                                    |