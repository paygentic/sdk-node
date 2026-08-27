# PriceProperties


## Supported Types

### `models.StandardPriceProperties`

```typescript
const value: models.StandardPriceProperties = {
  unitPrice: "<value>",
};
```

### `models.DynamicPriceProperties`

```typescript
const value: models.DynamicPriceProperties = {
  maxPrice: "<value>",
  minPrice: "<value>",
};
```

### `models.VolumePriceProperties`

```typescript
const value: models.VolumePriceProperties = {
  tiers: [
    {
      upTo: "<value>",
      unitPrice: "<value>",
    },
  ],
};
```

### `models.PercentagePriceProperties`

```typescript
const value: models.PercentagePriceProperties = {
  maxCharge: "<value>",
  minCharge: "<value>",
  percentage: "<value>",
};
```

