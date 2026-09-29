# Approval

## Example Usage

```typescript
import { Approval } from "@paygentic/sdk/models";

let value: Approval = {
  id: "<id>",
  object: "approval",
  merchantId: "<id>",
  resourceType: "invoice",
  resourceId: "<id>",
  kind: "data_review",
  decision: "rejected",
  requester: "<value>",
  dataSnapshotHash: "<value>",
  createdAt: new Date("2026-07-19T00:36:40.907Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.ApprovalObject](../models/approvalobject.md)                                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `resourceType`                                                                                | [models.ApprovalResourceType](../models/approvalresourcetype.md)                              | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `resourceId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `kind`                                                                                        | [models.ApprovalKind](../models/approvalkind.md)                                              | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `decision`                                                                                    | [models.ApprovalDecision](../models/approvaldecision.md)                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `requester`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `reviewer`                                                                                    | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `note`                                                                                        | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `dataSnapshotHash`                                                                            | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `decidedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |