# GroupBy

Group invoice data by dimension. Allowed values: 'plan' (max 5 groups, top 4 + 'other' when exceeding), 'customer' (max 25 groups, top 24 + 'other' when exceeding, sorted by revenue descending), 'currency' (one entry per currency, primary currency first then alphabetical). Note: groupBy values are mutually exclusive — combining them returns a 400 error. When groupBy=currency is active, top-level netRevenue, invoices, and payments fields are omitted; currencyBreakdown is the sole data source.

## Example Usage

```typescript
import { GroupBy } from "@paygentic/sdk/models/operations";

let value: GroupBy = "customer";
```

## Values

```typescript
"plan" | "customer" | "currency"
```