# MerchantIntegration

A merchant's tenant-level connection to an external provider via Ampersand.

## Example Usage

```typescript
import { MerchantIntegration } from "@paygentic/sdk/models";

let value: MerchantIntegration = {
  id: "<id>",
  merchantId: "<id>",
  provider: "salesforce",
  externalId: "<id>",
  status: "active",
  config: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  metadata: {},
  connectedAt: new Date("2025-07-16T13:58:11.821Z"),
  disconnectedAt: new Date("2026-05-03T03:46:02.434Z"),
  createdAt: new Date("2024-12-16T17:07:59.867Z"),
  updatedAt: new Date("2025-07-22T06:22:21.234Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a merchant integration                                                  |
| `object`                                                                                      | [models.MerchantIntegrationObject](../models/merchantintegrationobject.md)                    | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `provider`                                                                                    | [models.MerchantIntegrationProvider](../models/merchantintegrationprovider.md)                | :heavy_check_mark:                                                                            | External provider a merchant can connect at the tenant level                                  |
| `externalId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Ampersand installation id.                                                                    |
| `status`                                                                                      | [models.MerchantIntegrationStatus](../models/merchantintegrationstatus.md)                    | :heavy_check_mark:                                                                            | Connection lifecycle state. Live Ampersand health is separate and not stored here.            |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `connectedAt`                                                                                 | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `disconnectedAt`                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |