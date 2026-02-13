# ListEntitlementsResponse

Successfully retrieved the list of entitlements for the customer.

## Example Usage

```typescript
import { ListEntitlementsResponse } from "@paygentic/sdk/models/operations";

let value: ListEntitlementsResponse = {
  data: [],
  pagination: {},
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `object`                                                                               | [operations.ListEntitlementsObject](../../models/operations/listentitlementsobject.md) | :heavy_minus_sign:                                                                     | N/A                                                                                    |
| `data`                                                                                 | [models.EntitlementAccessResult](../../models/entitlementaccessresult.md)[]            | :heavy_check_mark:                                                                     | Array of entitlement access results.                                                   |
| `pagination`                                                                           | [models.OffsetPagination](../../models/offsetpagination.md)                            | :heavy_check_mark:                                                                     | Offset-based pagination response.                                                      |