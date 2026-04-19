# Code

Optional semantic business error code for machine-readable discrimination (e.g. 'TAX_NOT_ENABLED'). UPPER_SNAKE_CASE. Clients should check this field, not message.

## Example Usage

```typescript
import { Code } from "@paygentic/sdk/models";

let value: Code = "TAX_NOT_ENABLED";
```

## Values

```typescript
"TAX_NOT_ENABLED" | "PAYMENT_SESSION_EXPIRED"
```