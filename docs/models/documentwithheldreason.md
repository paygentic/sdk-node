# DocumentWithheldReason

Why no Paygentic-rendered document exists for this invoice, or null when none was withheld. A tax-registered merchant's document is a compliance artefact, so it is withheld unless the recorded tax reconciles with the provider exactly and the registered issuer identity is complete. Non-null therefore always accompanies pdfSource `tax_provider` or null, and never `paygentic`. Use it to tell a withheld document apart from an invoice the tax provider serves by design — both report pdfSource `tax_provider`, but only a withheld one can be repaired by POST /v2/invoices/{id}/generate-pdf. `tax_unreconciled`: the provider's tax figure was never recorded against this invoice. `issuer_identity_incomplete`: the registered legal name, tax ID or address could not be read. `tax_component_unpriceable`: a recorded tax component carried no presentable amount. `ledger_mismatch`: the recorded tax figures and the invoice's own totals disagree. `tax_provider_disagrees`: the provider re-read its filing and reported a different tax to the one this invoice was charged — terminal, because correcting an issued invoice is a credit note's job, so retrying the repair cannot clear it. New values may be added, so treat an unrecognised one as withheld rather than failing.

## Example Usage

```typescript
import { DocumentWithheldReason } from "@paygentic/sdk/models";

let value: DocumentWithheldReason = "ledger_mismatch";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"tax_unreconciled" | "issuer_identity_incomplete" | "tax_component_unpriceable" | "ledger_mismatch" | "tax_provider_disagrees" | Unrecognized<string>
```