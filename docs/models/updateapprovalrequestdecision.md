# UpdateApprovalRequestDecision

approved/rejected: reviewer decision (maker-checker enforced). cancelled: recall a pending approval or reopen an approved one.

## Example Usage

```typescript
import { UpdateApprovalRequestDecision } from "@paygentic/sdk/models";

let value: UpdateApprovalRequestDecision = "rejected";
```

## Values

```typescript
"approved" | "rejected" | "cancelled"
```