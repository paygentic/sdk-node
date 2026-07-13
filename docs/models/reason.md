# Reason

Coded failure reason. `grant_mint_failed` means the entitlement was created but its initial metered grant could not be minted; re-running this reconciliation retries the mint.

## Example Usage

```typescript
import { Reason } from "@paygentic/sdk/models";

let value: Reason = "grant_mint_failed";
```

## Values

```typescript
"entitlement_failed" | "grant_mint_failed"
```