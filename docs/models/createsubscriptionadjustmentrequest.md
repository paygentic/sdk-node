# CreateSubscriptionAdjustmentRequest

One adjustment to attach to the subscription. The type decides which number the body carries: a rate for percentageDiscount, a unit count and one target price for usageDiscount.


## Supported Types

### `models.CreatePercentageDiscountAdjustment`

```typescript
const value: models.CreatePercentageDiscountAdjustment = {
  type: "percentageDiscount",
  percentageDiscount: "<value>",
  effectiveFrom: new Date("2024-10-17T17:13:50.683Z"),
  idempotencyKey: "adj_fy26_growth_001",
};
```

### `models.CreateUsageDiscountAdjustment`

```typescript
const value: models.CreateUsageDiscountAdjustment = {
  type: "usageDiscount",
  usageDiscount: "<value>",
  targetPriceIds: [
    "<value 1>",
    "<value 2>",
  ],
  effectiveFrom: new Date("2024-06-08T04:02:18.330Z"),
  idempotencyKey: "adj_mar_outage_001",
};
```

