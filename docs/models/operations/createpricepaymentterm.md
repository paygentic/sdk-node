# CreatePricePaymentTerm

Billing timing preference. For billable metrics: 'instant' (charges immediately) or 'in_arrears' (charges at period end). For fees: 'in_advance' (charges upfront) or 'in_arrears' (charges at period end).

## Example Usage

```typescript
import { CreatePricePaymentTerm } from "@paygentic/sdk/models/operations";

let value: CreatePricePaymentTerm = "instant";
```

## Values

```typescript
"instant" | "in_arrears" | "in_advance"
```