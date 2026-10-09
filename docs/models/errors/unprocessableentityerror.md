# UnprocessableEntityError

`hosted_link` only: Paygentic cannot create a payment link. The `code` field gives the cause: `INVOICE_NOT_LINKABLE_STATUS` (the invoice is not `ISSUED` or `PAYMENT_FAILED`; do not retry), `INVOICE_NO_BALANCE` (no amount is unpaid; treat the invoice as paid), or `MERCHANT_NO_PAYMENT_ACCOUNT` (the merchant has no connected payment account; retry after onboarding is complete).

## Example Usage

```typescript
import { UnprocessableEntityError } from "@paygentic/sdk/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                                       | Type                                                                                        | Required                                                                                    | Description                                                                                 |
| ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `error`                                                                                     | *string*                                                                                    | :heavy_check_mark:                                                                          | Coarse HTTP error category (e.g. 'bad_request', 'forbidden'). Maps to the HTTP status code. |
| `message`                                                                                   | *string*                                                                                    | :heavy_check_mark:                                                                          | Human-readable error message. Clients must not parse this field programmatically.           |
| `code`                                                                                      | [models.InvoicePaymentLinkErrorCode](../../models/invoicepaymentlinkerrorcode.md)           | :heavy_check_mark:                                                                          | Why Paygentic cannot create a payment link for the invoice.                                 |
| `details`                                                                                   | Record<string, *any*>                                                                       | :heavy_minus_sign:                                                                          | Additional error details                                                                    |