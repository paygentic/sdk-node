# PaymentAwaitingApproval

Invoice 0 awaiting merchant approval before payment can proceed. The invoice is in DRAFT status with totals calculated. Approval is a platform-managed action and will be available via a public endpoint in a future release.

## Example Usage

```typescript
import { PaymentAwaitingApproval } from "@paygentic/sdk/models";

let value: PaymentAwaitingApproval = {
  invoiceId: "<id>",
  amount: "153.61",
  status: "awaiting_approval",
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `invoiceId`                                   | *string*                                      | :heavy_check_mark:                            | The Invoice 0 id awaiting approval            |
| `amount`                                      | *string*                                      | :heavy_check_mark:                            | Total payment amount in decimal dollar format |
| `status`                                      | *"awaiting_approval"*                         | :heavy_check_mark:                            | Payment status                                |