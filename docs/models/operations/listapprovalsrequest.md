# ListApprovalsRequest

## Example Usage

```typescript
import { ListApprovalsRequest } from "@paygentic/sdk/models/operations";

let value: ListApprovalsRequest = {};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `merchantId`                                                       | *string*                                                           | :heavy_minus_sign:                                                 | Filter by merchant                                                 |
| `resourceType`                                                     | [operations.ResourceType](../../models/operations/resourcetype.md) | :heavy_minus_sign:                                                 | Filter by resource type                                            |
| `resourceId`                                                       | *string*                                                           | :heavy_minus_sign:                                                 | Filter by resource id                                              |
| `kind`                                                             | [operations.Kind](../../models/operations/kind.md)                 | :heavy_minus_sign:                                                 | Filter by kind                                                     |
| `decision`                                                         | [operations.Decision](../../models/operations/decision.md)         | :heavy_minus_sign:                                                 | Filter by decision                                                 |
| `limit`                                                            | *number*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |
| `offset`                                                           | *number*                                                           | :heavy_minus_sign:                                                 | N/A                                                                |