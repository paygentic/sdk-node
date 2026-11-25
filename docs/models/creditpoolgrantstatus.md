# CreditPoolGrantStatus

Where the grant stands now. `active` grants have started and are neither expired nor voided; a fully used grant stays `active` with a `remainingBalance` of 0. `scheduled` grants start later. `expired` grants passed their expiry. `voided` grants were cancelled.

## Example Usage

```typescript
import { CreditPoolGrantStatus } from "@paygentic/sdk/models";

let value: CreditPoolGrantStatus = "scheduled";
```

## Values

```typescript
"active" | "scheduled" | "expired" | "voided"
```