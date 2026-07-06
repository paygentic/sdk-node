# SchemasApproval

## Example Usage

```typescript
import { SchemasApproval } from "@paygentic/sdk/models";

let value: SchemasApproval = {
  id: "<id>",
  object: "approval",
  merchantId: "<id>",
  resourceType: "order",
  resourceId: "<id>",
  kind: "push",
  decision: "pending",
  requester: "<value>",
  dataSnapshotHash: "<value>",
  createdAt: new Date("2025-01-19T04:20:38.690Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.SchemasApprovalObject](../models/schemasapprovalobject.md)                            | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `resourceType`                                                                                | [models.SchemasApprovalResourceType](../models/schemasapprovalresourcetype.md)                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `resourceId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `kind`                                                                                        | [models.SchemasApprovalKind](../models/schemasapprovalkind.md)                                | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `decision`                                                                                    | [models.SchemasApprovalDecision](../models/schemasapprovaldecision.md)                        | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `requester`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `reviewer`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `note`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `dataSnapshotHash`                                                                            | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `decidedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |