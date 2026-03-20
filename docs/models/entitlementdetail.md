# EntitlementDetail

A specific entitlement. The response shape varies by featureType.


## Supported Types

### `models.BooleanEntitlementDetail`

```typescript
const value: models.BooleanEntitlementDetail = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "boolean",
  status: "canceled",
  activeFrom: new Date("2024-07-14T18:32:18.901Z"),
  hasAccess: true,
};
```

### `models.StaticEntitlementDetail`

```typescript
const value: models.StaticEntitlementDetail = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "static",
  status: "canceled",
  activeFrom: new Date("2026-07-13T14:18:34.649Z"),
  hasAccess: true,
};
```

### `models.MeteredEntitlementDetail`

```typescript
const value: models.MeteredEntitlementDetail = {
  id: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "metered",
  status: "active",
  activeFrom: new Date("2025-08-02T04:33:12.548Z"),
  hasAccess: true,
  isSoftLimit: false,
  balance: 8984.39,
  usageInPeriod: 9117.79,
  overage: 6058.89,
};
```

