# ListMerchantIntegrationsResponse

List of merchant integrations

## Example Usage

```typescript
import { ListMerchantIntegrationsResponse } from "@paygentic/sdk/models/operations";

let value: ListMerchantIntegrationsResponse = {
  data: [
    {
      id: "<id>",
      merchantId: "<id>",
      provider: "accountsiq",
      capabilities: {
        resolvesItemCodes: true,
        sendsItemCodes: false,
      },
      externalId: "<id>",
      status: "error",
      config: {
        "key": "<value>",
      },
      metadata: {
        "key": "<value>",
        "key1": "<value>",
      },
      connectedAt: new Date("2025-03-18T11:32:10.780Z"),
      disconnectedAt: null,
      createdAt: new Date("2025-08-17T01:31:12.771Z"),
      updatedAt: new Date("2024-10-16T20:08:03.176Z"),
    },
  ],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `data`                                                              | [models.MerchantIntegration](../../models/merchantintegration.md)[] | :heavy_check_mark:                                                  | N/A                                                                 |
| `pagination`                                                        | [models.OffsetPagination](../../models/offsetpagination.md)         | :heavy_check_mark:                                                  | Offset-based pagination response.                                   |