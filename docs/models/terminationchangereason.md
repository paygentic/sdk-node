# TerminationChangeReason

Why the subscription was terminated. Null while it is not terminated.

## Example Usage

```typescript
import { TerminationChangeReason } from "@paygentic/sdk/models";

let value: TerminationChangeReason = "unspecified";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"commercial" | "correction" | "migration" | "unspecified" | Unrecognized<string>
```