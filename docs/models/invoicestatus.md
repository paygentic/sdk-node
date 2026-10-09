# InvoiceStatus

The current status of the invoice. PROJECTED is returned only by GET /v2/invoices/projected and is never the status of a stored invoice.

## Example Usage

```typescript
import { InvoiceStatus } from "@paygentic/sdk/models";

let value: InvoiceStatus = "DRAFT";
```

## Values

```typescript
"ACTIVE" | "CLOSING" | "CLOSED" | "CALCULATING" | "DRAFT" | "ISSUED" | "PAYMENT_FAILED" | "PAID" | "CANCELLED" | "WRITTEN_OFF" | "FAILED" | "PROJECTED"
```