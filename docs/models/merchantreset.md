# MerchantReset

What the reset deletes. Every field of the chosen shape is required, so each call says what goes.


## Supported Types

### `models.MerchantScope`

```typescript
const value: models.MerchantScope = {
  scope: "merchant",
  keepCatalog: true,
};
```

### `models.CustomerScope`

```typescript
const value: models.CustomerScope = {
  scope: "customer",
  customerId: "<id>",
};
```

