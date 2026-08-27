# DynamicPriceProperties

Dynamic pricing model

## Example Usage

```typescript
import { DynamicPriceProperties } from "@paygentic/sdk/models";

let value: DynamicPriceProperties = {
  maxPrice: "<value>",
  minPrice: "<value>",
};
```

## Fields

| Field                                                                                                                                 | Type                                                                                                                                  | Required                                                                                                                              | Description                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `maxPrice`                                                                                                                            | *string*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Upper limit of the price range for dynamic pricing. Sample values: '0.10' means $0.10 per token for large volumes at peak times       |
| `minPrice`                                                                                                                            | *string*                                                                                                                              | :heavy_check_mark:                                                                                                                    | Lower limit of the price range for dynamic pricing. Sample values: '0.01' means $0.01 per token for low volumes during off-peak hours |