# SubscriptionVersionPolicy

How the subscription follows new versions of its plan. `floating` follows the plan's default version: when the default changes, the subscription bills from the new default from its next billing period. `pinned` keeps the plan version that the subscription holds. A subscription created without a value is `floating`. A change to this value does not change a billing period that has already started.

## Example Usage

```typescript
import { SubscriptionVersionPolicy } from "@paygentic/sdk/models";

let value: SubscriptionVersionPolicy = "floating";
```

## Values

```typescript
"floating" | "pinned"
```