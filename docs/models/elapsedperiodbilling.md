# ElapsedPeriodBilling

Whether a backdated start bills its elapsed periods. A start is backdated when `startedAt` is more than 24 hours before the subscription is created. `none` bills only charges that fall due from the moment of creation, for a customer whose earlier periods another system already billed. `per_period` bills every charge that fell due from `startedAt`, on one first invoice; it refuses a `startedAt` more than 12 months back. Has no effect on a start that is not backdated. Defaults to `none`.

## Example Usage

```typescript
import { ElapsedPeriodBilling } from "@paygentic/sdk/models";

let value: ElapsedPeriodBilling = "per_period";
```

## Values

```typescript
"none" | "per_period"
```