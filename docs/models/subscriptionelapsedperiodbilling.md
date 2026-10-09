# SubscriptionElapsedPeriodBilling

Whether this subscription's backdated start bills its elapsed periods, as chosen at creation. `null` for a subscription created before the choice existed. `null` is listed in the enum as well as via `nullable` because the response validator checks the enum independently.

## Example Usage

```typescript
import { SubscriptionElapsedPeriodBilling } from "@paygentic/sdk/models";

let value: SubscriptionElapsedPeriodBilling = "per_period";
```

## Values

```typescript
"none" | "per_period"
```