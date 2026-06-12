# UpsertMerchantIntegrationRequest

## Example Usage

```typescript
import { UpsertMerchantIntegrationRequest } from "@paygentic/sdk/models/operations";

let value: UpsertMerchantIntegrationRequest = {
  merchantId: "<id>",
  provider: "salesforce",
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `merchantId`                                                                       | *string*                                                                           | :heavy_check_mark:                                                                 | Unique identifier for an organization                                              |
| `provider`                                                                         | [models.MerchantIntegrationProvider](../../models/merchantintegrationprovider.md)  | :heavy_check_mark:                                                                 | External provider a merchant can connect at the tenant level                       |
| `externalId`                                                                       | *string*                                                                           | :heavy_minus_sign:                                                                 | Ampersand installation id.                                                         |
| `status`                                                                           | [models.MerchantIntegrationStatus](../../models/merchantintegrationstatus.md)      | :heavy_minus_sign:                                                                 | Connection lifecycle state. Live Ampersand health is separate and not stored here. |
| `config`                                                                           | Record<string, *any*>                                                              | :heavy_minus_sign:                                                                 | N/A                                                                                |
| `metadata`                                                                         | Record<string, *any*>                                                              | :heavy_minus_sign:                                                                 | N/A                                                                                |