# MerchantScope

## Example Usage

```typescript
import { MerchantScope } from "@paygentic/sdk/models";

let value: MerchantScope = {
  scope: "merchant",
  keepCatalog: true,
};
```

## Fields

| Field                                                                                                                                                                          | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `scope`                                                                                                                                                                        | *"merchant"*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                             | N/A                                                                                                                                                                            |
| `keepCatalog`                                                                                                                                                                  | *boolean*                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                             | `false` also deletes the catalog: products, plans, plan versions, prices, fees, features, billable metrics, pricing units, items, costs and sources, back to an empty account. |