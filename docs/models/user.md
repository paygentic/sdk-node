# User

## Example Usage

```typescript
import { User } from "@paygentic/sdk/models";

let value: User = {
  id: "<id>",
  createdAt: new Date("2025-07-05T21:57:00.508Z"),
  email: "Jackie43@gmail.com",
  organizations: [],
  oryId: "<id>",
  updatedAt: new Date("2026-04-22T20:08:46.899Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a user                                                                  |
| `object`                                                                                      | [models.UserObject](../models/userobject.md)                                                  | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `address`                                                                                     | [models.Address](../models/address.md)                                                        | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `dateOfBirth`                                                                                 | [RFCDate](../types/rfcdate.md)                                                                | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `email`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `firstName`                                                                                   | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `lastName`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `organizations`                                                                               | [models.UserOrganization](../models/userorganization.md)[]                                    | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `oryId`                                                                                       | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `phone`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.UserType](../models/usertype.md)                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |