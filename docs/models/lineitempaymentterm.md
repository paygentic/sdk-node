# LineItemPaymentTerm

Payment term for fee items. Null for metered/manual lines. `null` is listed in the enum as well as via `nullable` because OpenAPI 3.0 validators check the enum independently — `nullable: true` alone does not admit it, and createLineItem (which always returns null here) was emitting a schema-violating body.

## Example Usage

```typescript
import { LineItemPaymentTerm } from "@paygentic/sdk/models";

let value: LineItemPaymentTerm = "in_advance";
```

## Values

```typescript
"in_advance" | "in_arrears"
```