# CreatePlanBillingCadence

ISO 8601 duration for the billing period. Takes precedence over billingInterval when both are provided.

## Example Usage

```typescript
import { CreatePlanBillingCadence } from "@paygentic/sdk/models/operations";

let value: CreatePlanBillingCadence = "P3M";
```

## Values

```typescript
"P1M" | "P3M" | "P1Y"
```