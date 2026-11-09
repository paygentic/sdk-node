# EntityType

The type of Paygentic entity this external reference points at. `subscriptionProposal` and `subscription` references link a subscription proposal, and the subscription its approval creates, to the CRM record they come from. They are read-only through these endpoints.

## Example Usage

```typescript
import { EntityType } from "@paygentic/sdk/models";

let value: EntityType = "item";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"item" | "customer" | "subscriptionProposal" | "subscription" | Unrecognized<string>
```