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
      provider: "salesforce",
      externalId: "<id>",
      status: "disconnected",
      config: {
        "key": "<value>",
        "key1": "<value>",
        "key2": "<value>",
      },
      metadata: {
        "key": "<value>",
      },
      connectedAt: new Date("2025-09-15T17:12:16.525Z"),
      disconnectedAt: new Date("2024-03-24T08:28:07.211Z"),
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