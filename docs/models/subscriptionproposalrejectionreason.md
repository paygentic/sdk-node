# SubscriptionProposalRejectionReason

Why a person rejected the proposal. `price_mismatch`: a price or discount is not the one agreed. `wrong_plan`: the proposal names the wrong plan. `wrong_start_date`: the start date is wrong. `wrong_customer`: the proposal names the wrong customer. `duplicate`: the customer already has this subscription, or another proposal holds it. `other`: another reason, explained in `text`.

## Example Usage

```typescript
import { SubscriptionProposalRejectionReason } from "@paygentic/sdk/models";

let value: SubscriptionProposalRejectionReason = "price_mismatch";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"price_mismatch" | "wrong_plan" | "wrong_start_date" | "wrong_customer" | "duplicate" | "other" | Unrecognized<string>
```