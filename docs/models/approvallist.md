# ApprovalList

## Example Usage

```typescript
import { ApprovalList } from "@paygentic/sdk/models";

let value: ApprovalList = {
  object: "list",
  data: [
    {
      id: "<id>",
      object: "approval",
      merchantId: "<id>",
      resourceType: "invoice",
      resourceId: "<id>",
      kind: "financial_review",
      decision: "approved",
      requester: "<value>",
      dataSnapshotHash: "<value>",
      createdAt: new Date("2024-08-27T11:53:38.054Z"),
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

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `object`                                                     | [models.ApprovalListObject](../models/approvallistobject.md) | :heavy_check_mark:                                           | N/A                                                          |
| `data`                                                       | [models.SchemasApproval](../models/schemasapproval.md)[]     | :heavy_check_mark:                                           | N/A                                                          |
| `pagination`                                                 | [models.OffsetPagination](../models/offsetpagination.md)     | :heavy_check_mark:                                           | Offset-based pagination response.                            |