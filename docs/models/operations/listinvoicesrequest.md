# ListInvoicesRequest

## Example Usage

```typescript
import { ListInvoicesRequest } from "@paygentic/sdk/models/operations";

let value: ListInvoicesRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `limit`                                                                        | *number*                                                                       | :heavy_minus_sign:                                                             | Maximum number of invoices to return                                           |
| `nextActionAt`                                                                 | [operations.NextActionAt](../../models/operations/nextactionat.md)             | :heavy_minus_sign:                                                             | Filter for invoices ready for processing (platform only)                       |
| `status`                                                                       | [operations.ListInvoicesStatus](../../models/operations/listinvoicesstatus.md) | :heavy_minus_sign:                                                             | Filter invoices by status                                                      |
| `subscriptionId`                                                               | *string*                                                                       | :heavy_minus_sign:                                                             | Filter invoices by subscription ID                                             |