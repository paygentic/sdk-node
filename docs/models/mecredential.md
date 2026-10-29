# MeCredential

The credential of the call. clientId is set for an OAuth token and apiKeyId for an API key.

## Example Usage

```typescript
import { MeCredential } from "@paygentic/sdk/models";

let value: MeCredential = {
  type: "oauth",
};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `type`                                                   | [models.MeCredentialType](../models/mecredentialtype.md) | :heavy_check_mark:                                       | N/A                                                      |
| `clientId`                                               | *string*                                                 | :heavy_minus_sign:                                       | The OAuth client of the token.                           |
| `apiKeyId`                                               | *string*                                                 | :heavy_minus_sign:                                       | The API key of the call.                                 |