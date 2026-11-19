# SubscriptionProposalDecisionDecision

`approve` creates the subscription and makes the proposal `approved`. `reject` rejects the proposal. Either is final: the proposal never becomes `pending` again.

## Example Usage

```typescript
import { SubscriptionProposalDecisionDecision } from "@paygentic/sdk/models";

let value: SubscriptionProposalDecisionDecision = "reject";
```

## Values

```typescript
"approve" | "reject"
```