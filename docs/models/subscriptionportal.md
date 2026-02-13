# SubscriptionPortal

## Example Usage

```typescript
import { SubscriptionPortal } from "@paygentic/sdk/models";

let value: SubscriptionPortal = {
  object: "subscriptionPortal",
  expiresAt: new Date("2024-04-06T11:37:43.654Z"),
  url: "https://scary-apparatus.net/",
};
```

## Fields

| Field                                                                                                                                                                                  | Type                                                                                                                                                                                   | Required                                                                                                                                                                               | Description                                                                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                                                                                               | [models.SubscriptionPortalObject](../models/subscriptionportalobject.md)                                                                                                               | :heavy_check_mark:                                                                                                                                                                     | N/A                                                                                                                                                                                    |
| `expiresAt`                                                                                                                                                                            | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                          | :heavy_check_mark:                                                                                                                                                                     | Portal link expiration timestamp in ISO 8601 format. Sample values: '2024-01-15T23:59:59Z', '2024-02-01T12:00:00Z'                                                                     |
| `url`                                                                                                                                                                                  | *string*                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                     | Secure portal access URL for customer subscription management. Sample values: 'https://portal.paygentic.com/sub/abc123?token=xyz789', 'https://customer.example.com/portal/sub_456def' |