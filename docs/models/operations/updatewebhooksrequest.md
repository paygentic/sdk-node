# UpdateWebhooksRequest

## Example Usage

```typescript
import { UpdateWebhooksRequest } from "@paygentic/sdk/models/operations";

let value: UpdateWebhooksRequest = {
  requestBody: {
    enabled: false,
  },
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `merchantId`                                                                                                  | *string*                                                                                                      | :heavy_minus_sign:                                                                                            | The merchant organization ID. If omitted, defaults to the merchant associated with the authenticated API key. |
| `requestBody`                                                                                                 | [operations.UpdateWebhooksRequestBody](../../models/operations/updatewebhooksrequestbody.md)                  | :heavy_check_mark:                                                                                            | N/A                                                                                                           |