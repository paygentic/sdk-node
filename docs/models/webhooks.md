# Webhooks

## Example Usage

```typescript
import { Webhooks } from "@paygentic/sdk/models";

let value: Webhooks = {
  object: "webhooks",
  applicationId: "<id>",
  createdAt: new Date("2025-03-18T12:39:09.752Z"),
  enabled: false,
  merchantId: "<id>",
  updatedAt: new Date("2025-01-11T10:44:55.721Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.WebhooksObject](../models/webhooksobject.md)                                          | :heavy_check_mark:                                                                            | Object type identifier                                                                        |
| `applicationId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | Svix application identifier                                                                   |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When webhooks were first enabled                                                              |
| `enabled`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | Whether webhooks are enabled                                                                  |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Merchant identifier                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When webhooks were last updated                                                               |