# ChangeReason

Why a change was made. `correction` repairs data that was entered wrong; `migration` moves a contract from another system; `commercial` is a real change to the deal; `contractual` applies a step the original contract scheduled, such as an annual uplift. Defaults to `unspecified`.

## Example Usage

```typescript
import { ChangeReason } from "@paygentic/sdk/models";

let value: ChangeReason = "correction";

// Open enum: unrecognized values are captured as Unrecognized<string>
```

## Values

```typescript
"commercial" | "correction" | "migration" | "unspecified" | "contractual" | Unrecognized<string>
```