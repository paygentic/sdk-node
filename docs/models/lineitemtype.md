# LineItemType

The type of line item. 'discount' line items represent grant discounts with negative subtotal/total amounts.

## Example Usage

```typescript
import { LineItemType } from "@paygentic/sdk/models";

let value: LineItemType = "metered";
```

## Values

```typescript
"fee" | "metered" | "manual" | "discount"
```