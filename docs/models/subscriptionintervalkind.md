# SubscriptionIntervalKind

plan_line if the plan version has a line with this priceKey. subscription_owned if it does not, so the interval belongs to this subscription only. After an add, check the kind. A mistyped priceKey creates a subscription_owned interval.

## Example Usage

```typescript
import { SubscriptionIntervalKind } from "@paygentic/sdk/models";

let value: SubscriptionIntervalKind = "subscription_owned";
```

## Values

```typescript
"plan_line" | "subscription_owned"
```