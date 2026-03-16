# ListEntitlementGrantsRequest

## Example Usage

```typescript
import { ListEntitlementGrantsRequest } from "@paygentic/sdk/models/operations";

let value: ListEntitlementGrantsRequest = {
  entitlementId: "<id>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `entitlementId`                                        | *string*                                               | :heavy_check_mark:                                     | The unique identifier of the entitlement.              |
| `limit`                                                | *number*                                               | :heavy_minus_sign:                                     | Maximum number of grants to return per page.           |
| `offset`                                               | *number*                                               | :heavy_minus_sign:                                     | Number of grants to skip.                              |
| `includeVoided`                                        | *boolean*                                              | :heavy_minus_sign:                                     | When true, voided grants are included in the response. |