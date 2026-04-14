# EventType

Type of event: 'usage' for billable metric events, 'fee' for fee events, 'discount' for grant discount line items (subtotal/total are negative, representing a credit)

## Example Usage

```typescript
import { EventType } from "@paygentic/sdk/models";

let value: EventType = "fee";
```

## Values

```typescript
"usage" | "fee" | "discount"
```