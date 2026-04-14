# ListEntitlementGrantsResponse

Successfully retrieved the list of grants.

## Example Usage

```typescript
import { ListEntitlementGrantsResponse } from "@paygentic/sdk/models/operations";

let value: ListEntitlementGrantsResponse = {
  data: [
    {
      id: "<id>",
      entitlementId: "<id>",
      amount: 398.2,
      effectiveAt: new Date("2024-04-27T22:31:40.007Z"),
      createdAt: new Date("2024-11-16T08:19:23.748Z"),
      recurrencePeriod: "<value>",
      idempotencyKey: "<value>",
    },
  ],
  pagination: {},
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `object`                                                                                         | [operations.ListEntitlementGrantsObject](../../models/operations/listentitlementgrantsobject.md) | :heavy_minus_sign:                                                                               | N/A                                                                                              |
| `data`                                                                                           | [models.Grant](../../models/grant.md)[]                                                          | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `pagination`                                                                                     | [models.OffsetPagination](../../models/offsetpagination.md)                                      | :heavy_check_mark:                                                                               | Offset-based pagination response.                                                                |