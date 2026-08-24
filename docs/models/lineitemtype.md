# LineItemType

The type of line item. 'discount' and 'adjustment' line items have negative subtotal/total amounts: 'discount' is a grant discount, 'adjustment' is a discount agreed on the subscription.

## Example Usage

```typescript
import { LineItemType } from "@paygentic/sdk/models";

let value: LineItemType = "metered";
```

## Values

```typescript
"fee" | "metered" | "manual" | "discount" | "adjustment"
```