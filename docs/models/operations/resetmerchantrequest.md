# ResetMerchantRequest

## Example Usage

```typescript
import { ResetMerchantRequest } from "@paygentic/sdk/models/operations";

let value: ResetMerchantRequest = {
  merchantId: "<id>",
  merchantReset: {
    scope: "merchant",
    keepCatalog: false,
  },
};
```

## Fields

| Field                  | Type                   | Required               | Description            |
| ---------------------- | ---------------------- | ---------------------- | ---------------------- |
| `merchantId`           | *string*               | :heavy_check_mark:     | N/A                    |
| `merchantReset`        | *models.MerchantReset* | :heavy_check_mark:     | N/A                    |