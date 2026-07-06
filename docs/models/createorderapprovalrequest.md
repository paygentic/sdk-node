# CreateOrderApprovalRequest

## Example Usage

```typescript
import { CreateOrderApprovalRequest } from "@paygentic/sdk/models";

let value: CreateOrderApprovalRequest = {};
```

## Fields

| Field                                                                                                                          | Type                                                                                                                           | Required                                                                                                                       | Description                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------ |
| `requester`                                                                                                                    | *string*                                                                                                                       | :heavy_minus_sign:                                                                                                             | Optional. The maker submitting the order. Derived from the authenticated principal; only a platform key may set it explicitly. |
| `note`                                                                                                                         | *string*                                                                                                                       | :heavy_minus_sign:                                                                                                             | N/A                                                                                                                            |