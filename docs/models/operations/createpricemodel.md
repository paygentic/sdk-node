# CreatePriceModel

Pricing calculation model. Required for billable metrics, optional for fees (defaults to 'standard').

## Example Usage

```typescript
import { CreatePriceModel } from "@paygentic/sdk/models/operations";

let value: CreatePriceModel = "volume";
```

## Values

```typescript
"standard" | "dynamic" | "volume" | "percentage"
```