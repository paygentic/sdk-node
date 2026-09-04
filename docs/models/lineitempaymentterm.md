# LineItemPaymentTerm

When the line falls due relative to the window it covers. A fee line carries its price's term; a metered line is stamped `in_arrears`, though metered rows predating that rule carry `null`. Manual, grant-discount and adjustment lines are billed on no term of their own and are `null`. `null` is listed in the enum as well as via `nullable` because OpenAPI 3.0 validators check the enum independently — `nullable: true` alone does not admit it, and createLineItem (which always returns null here) was emitting a schema-violating body.

## Example Usage

```typescript
import { LineItemPaymentTerm } from "@paygentic/sdk/models";

let value: LineItemPaymentTerm = "in_advance";
```

## Values

```typescript
"in_advance" | "in_arrears"
```