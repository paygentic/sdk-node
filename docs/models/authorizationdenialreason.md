# AuthorizationDenialReason

Present on a 403 from the authorization check. Says why access was refused: the caller has no role that grants the permission, the OAuth token lacks the scope, or the caller is not a member of the organization.

## Example Usage

```typescript
import { AuthorizationDenialReason } from "@paygentic/sdk/models";

let value: AuthorizationDenialReason = "not_member";
```

## Values

```typescript
"no_permission" | "insufficient_scope" | "not_member"
```