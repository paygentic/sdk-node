# CreateSubscriptionAdjustmentRequest

One adjustment to attach to the subscription. The type decides which number the body carries: a rate for percentageDiscount, a unit count and one target price for usageDiscount, and a contracted quantity and one target price for minimumQuantity and maximumQuantity.


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

### `models.CreateMinimumQuantityAdjustment`

```typescript
const value: models.CreateMinimumQuantityAdjustment = {
  type: "minimumQuantity",
  minimumQuantity: "<value>",
  targetPriceIds: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  effectiveFrom: new Date("2024-07-21T06:44:54.904Z"),
  idempotencyKey: "adj_fortress_seats_001",
};
```

### `models.CreateMaximumQuantityAdjustment`

```typescript
const value: models.CreateMaximumQuantityAdjustment = {
  type: "maximumQuantity",
  maximumQuantity: "<value>",
  targetPriceIds: [
    "<value 1>",
    "<value 2>",
    "<value 3>",
  ],
  effectiveFrom: new Date("2024-05-25T19:27:17.739Z"),
  idempotencyKey: "adj_fortress_seats_001",
};
```

