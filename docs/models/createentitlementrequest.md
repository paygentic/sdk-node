# CreateEntitlementRequest

## Example Usage

```typescript
import { CreateEntitlementRequest } from "@paygentic/sdk/models";

let value: CreateEntitlementRequest = {
  customerId: "<id>",
  entitlementData: [],
  merchantId: "<id>",
};
```

## Fields

| Field                                                                                                                                  | Type                                                                                                                                   | Required                                                                                                                               | Description                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `customerId`                                                                                                                           | *string*                                                                                                                               | :heavy_check_mark:                                                                                                                     | Unique identifier for a customer                                                                                                       |
| `entitlementData`                                                                                                                      | [models.EntitlementDatum](../models/entitlementdatum.md)[]                                                                             | :heavy_check_mark:                                                                                                                     | Array of consumption metrics with quantities to pre-authorize payment for.                                                             |
| `maxUses`                                                                                                                              | *number*                                                                                                                               | :heavy_minus_sign:                                                                                                                     | Maximum consumption events allowed before expiration (optional). Defaults to 1 for global entitlements, 100 for regional entitlements. |
| `merchantId`                                                                                                                           | *string*                                                                                                                               | :heavy_check_mark:                                                                                                                     | Unique identifier for a merchant/organization                                                                                          |