# SubscriptionProposalConflictCode

Why a proposal route answered 409. `RESYNC_CONFLICT`: a re-sync changed a field a person amended; stop, a person rejects and the CRM sends again. `ALREADY_APPROVED`: the proposal is approved; stop. `NOT_PENDING`: the proposal is decided; stop. `CHANGED`: the proposal changed since it was read; read it again and retry. `DUPLICATE`: the customer already has a live subscription for the product; reject the proposal. `INVALID`: the proposal now fails a check of subscription create; amend or reject it. Open set: approve can pass on a conflict of subscription create with that conflict's own code, so treat any other code as an unhandled conflict.

## Example Usage

```typescript
import { SubscriptionProposalConflictCode } from "@paygentic/sdk/models";

let value: SubscriptionProposalConflictCode = "SUBSCRIPTION_PROPOSAL_DUPLICATE";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"SUBSCRIPTION_PROPOSAL_RESYNC_CONFLICT" | "SUBSCRIPTION_PROPOSAL_ALREADY_APPROVED" | "SUBSCRIPTION_PROPOSAL_NOT_PENDING" | "SUBSCRIPTION_PROPOSAL_CHANGED" | "SUBSCRIPTION_PROPOSAL_DUPLICATE" | "SUBSCRIPTION_PROPOSAL_INVALID" | Unrecognized<string>
```