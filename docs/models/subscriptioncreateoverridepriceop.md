# SubscriptionCreateOverridePriceOp

A rate or quantity override for a price the plan version carries. Supply at least one of unitPrice or baseQuantity; a request supplying neither is rejected with a 400 naming the entry.

## Example Usage

```typescript
import { SubscriptionCreateOverridePriceOp } from "@paygentic/sdk/models";

let value: SubscriptionCreateOverridePriceOp = {
  overridesPriceId: "<id>",
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `overridesPriceId`                                                          | *string*                                                                    | :heavy_check_mark:                                                          | The plan-version price being overridden. Its priceKey lineage is preserved. |
| `unitPrice`                                                                 | *string*                                                                    | :heavy_minus_sign:                                                          | The agreed rate, as a decimal string.                                       |
| `baseQuantity`                                                              | *string*                                                                    | :heavy_minus_sign:                                                          | The agreed quantity, as a decimal string.                                   |