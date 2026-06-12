# ListMerchantIntegrationsRequest

## Example Usage

```typescript
import { ListMerchantIntegrationsRequest } from "@paygentic/sdk/models/operations";

let value: ListMerchantIntegrationsRequest = {};
```

## Fields

| Field                                                                             | Type                                                                              | Required                                                                          | Description                                                                       |
| --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- |
| `merchantId`                                                                      | *string*                                                                          | :heavy_minus_sign:                                                                | Restrict results to a specific merchant. All active filters AND together.         |
| `provider`                                                                        | [models.MerchantIntegrationProvider](../../models/merchantintegrationprovider.md) | :heavy_minus_sign:                                                                | Filter by provider (e.g. `salesforce`).                                           |
| `limit`                                                                           | *number*                                                                          | :heavy_minus_sign:                                                                | N/A                                                                               |
| `offset`                                                                          | *number*                                                                          | :heavy_minus_sign:                                                                | N/A                                                                               |