# InvoiceLineItemPaymentTerm

When this line falls due relative to the window it covers: `in_advance` at the window's start, `in_arrears` at its end. A metered line is stamped `in_arrears`, because usage is only known once the window closes — but metered rows written before that rule carry `null` and were never backfilled, so do not read a metered line's term as guaranteed. `null` also means the line is not billed on a term of its own: manual, grant-discount and adjustment lines carry no term, and an adjustment instead falls due with the charge it reduces. Treat `null` as an expected value on any line type, not an error.

## Example Usage

```typescript
import { InvoiceLineItemPaymentTerm } from "@paygentic/sdk/models";

let value: InvoiceLineItemPaymentTerm = "in_advance";
```

## Values

```typescript
"in_advance" | "in_arrears"
```