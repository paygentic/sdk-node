# Timing

When the migration takes effect. `next_period` moves everything at the end of the current billing period. `immediate` changes entitlements at once, bills in-arrears prices for the whole current period at the target version, and changes in-advance prices at the end of the current period. Neither prorates. If absent, the plan's versionTransition applies.

## Example Usage

```typescript
import { Timing } from "@paygentic/sdk/models";

let value: Timing = "immediate";
```

## Values

```typescript
"next_period" | "immediate"
```