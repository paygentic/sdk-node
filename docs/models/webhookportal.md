# WebhookPortal

## Example Usage

```typescript
import { WebhookPortal } from "@paygentic/sdk/models";

let value: WebhookPortal = {
  object: "webhookPortal",
  expiresAt: new Date("2024-07-06T22:16:23.098Z"),
  url: "https://free-drug.net/",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `object`                                                                                      | [models.WebhookPortalObject](../models/webhookportalobject.md)                                | :heavy_check_mark:                                                                            | Object type identifier                                                                        |
| `expiresAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | When the portal link expires                                                                  |
| `url`                                                                                         | *string*                                                                                      | :heavy_check_mark:                                                                            | Magic link URL to access the webhook portal                                                   |