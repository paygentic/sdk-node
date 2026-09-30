# PeriodBasis

Which date places revenue inside the window. 'issued' (default) counts whole invoices by their issue date, the basis revenue is recognised on. 'billingPeriod' counts invoice lines by the start of the period each line bills, so a window covering one billing period returns that period's charges, whichever invoices carry them: this month's advance fee and this month's arrears usage. Paid, outstanding and written-off follow each line's invoice; a refund splits across its invoice's lines by subtotal; payments not tied to an invoice are excluded because they bill no period.

## Example Usage

```typescript
import { PeriodBasis } from "@paygentic/sdk/models/operations";

let value: PeriodBasis = "billingPeriod";
```

## Values

```typescript
"issued" | "billingPeriod"
```