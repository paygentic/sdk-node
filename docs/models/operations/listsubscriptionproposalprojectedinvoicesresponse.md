# ListSubscriptionProposalProjectedInvoicesResponse

The invoices approving the proposal now would raise, earliest first

## Example Usage

```typescript
import { ListSubscriptionProposalProjectedInvoicesResponse } from "@paygentic/sdk/models/operations";

let value: ListSubscriptionProposalProjectedInvoicesResponse = {
  object: "list",
  data: [],
  pagination: {
    limit: 513451,
    offset: 150252,
    total: 898024,
  },
};
```

## Fields

| Field                                                                                                                                    | Type                                                                                                                                     | Required                                                                                                                                 | Description                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                                                 | [operations.ListSubscriptionProposalProjectedInvoicesObject](../../models/operations/listsubscriptionproposalprojectedinvoicesobject.md) | :heavy_check_mark:                                                                                                                       | N/A                                                                                                                                      |
| `data`                                                                                                                                   | [models.Invoice](../../models/invoice.md)[]                                                                                              | :heavy_check_mark:                                                                                                                       | N/A                                                                                                                                      |
| `pagination`                                                                                                                             | [models.OffsetPagination](../../models/offsetpagination.md)                                                                              | :heavy_check_mark:                                                                                                                       | Offset-based pagination response.                                                                                                        |