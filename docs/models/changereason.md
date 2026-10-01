# ChangeReason

Why a change was made. `correction` fixes data to match what was agreed; `migration` moves a contract from another system; `commercial` is a real change to the deal. Defaults to `unspecified`.

## Example Usage

```typescript
import { ChangeReason } from "@paygentic/sdk/models";

let value: ChangeReason = "correction";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"commercial" | "correction" | "migration" | "unspecified" | Unrecognized<string>
```