# Me

## Example Usage

```typescript
import { Me } from "@paygentic/sdk/models";

let value: Me = {
  userId: "<id>",
  organizationId: "<id>",
  organizationType: "merchant",
  roles: [
    "<value 1>",
    "<value 2>",
  ],
  permissions: [],
  credential: {
    type: "apiKey",
  },
};
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `userId`                                                                                    | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `organizationId`                                                                            | *string*                                                                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `organizationType`                                                                          | [models.OrganizationType](../models/organizationtype.md)                                    | :heavy_check_mark:                                                                          | N/A                                                                                         |
| `roles`                                                                                     | *string*[]                                                                                  | :heavy_check_mark:                                                                          | The role names of the caller in the active organization.                                    |
| `permissions`                                                                               | [models.Permission](../models/permission.md)[]                                              | :heavy_check_mark:                                                                          | The permissions that the credential of the call holds in the active organization.           |
| `credential`                                                                                | [models.MeCredential](../models/mecredential.md)                                            | :heavy_check_mark:                                                                          | The credential of the call. clientId is set for an OAuth token and apiKeyId for an API key. |