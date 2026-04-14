# UpdatePlanBillingCadence

ISO 8601 duration for the billing period. Takes precedence over billingInterval when both are provided.

## Example Usage

```typescript
import { UpdatePlanBillingCadence } from "@paygentic/sdk/models/operations";

let value: UpdatePlanBillingCadence = "P1M";
```

## Values

```typescript
"P1M" | "P3M" | "P1Y"
```