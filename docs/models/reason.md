# Reason

Coded failure reason. `entitlement_failed` means the entitlement itself could not be created. `grant_mint_failed` means the entitlement was created but its initial metered grant could not be minted; re-running this reconciliation retries the mint. `reset_cycle_misaligned` means the feature grants a credit discount on a reset cycle that is not the window it would be billed on, so re-running cannot succeed until the plan or the price is corrected.

## Example Usage

```typescript
import { Reason } from "@paygentic/sdk/models";

let value: Reason = "reset_cycle_misaligned";
```

## Values

```typescript
"entitlement_failed" | "grant_mint_failed" | "reset_cycle_misaligned"
```