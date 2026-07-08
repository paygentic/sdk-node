# EntitlementListItem

An entitlement as returned by the list endpoint. The shape varies by featureType. Uses `entitlementId` (not `id`) for backwards compatibility with the original list contract.


## Supported Types

### `models.BooleanEntitlementListItem`

```typescript
const value: models.BooleanEntitlementListItem = {
  entitlementId: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "boolean",
  productId: "<id>",
  subscriptionId: "<id>",
  status: "canceled",
  activeFrom: new Date("2026-04-27T17:56:46.611Z"),
  activeTo: null,
  hasAccess: false,
  metadata: {
    "key": "<value>",
  },
  config: {
    "key": "<value>",
  },
};
```

### `models.StaticEntitlementListItem`

```typescript
const value: models.StaticEntitlementListItem = {
  entitlementId: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "static",
  productId: "<id>",
  subscriptionId: null,
  status: "active",
  activeFrom: new Date("2026-03-27T08:08:50.344Z"),
  activeTo: new Date("2024-06-14T21:02:55.215Z"),
  hasAccess: true,
  metadata: {
    "key": "<value>",
    "key1": "<value>",
  },
  config: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
};
```

### `models.MeteredEntitlementListItem`

```typescript
const value: models.MeteredEntitlementListItem = {
  entitlementId: "<id>",
  customerId: "<id>",
  featureId: "<id>",
  featureKey: "<value>",
  featureType: "metered",
  productId: "<id>",
  subscriptionId: "<id>",
  status: "expired",
  activeFrom: new Date("2026-07-03T01:54:25.246Z"),
  activeTo: new Date("2025-02-25T03:55:15.551Z"),
  hasAccess: true,
  metadata: {
    "key": "<value>",
    "key1": "<value>",
  },
  config: {
    "key": "<value>",
  },
  isSoftLimit: false,
  balance: 3186.94,
  usageInPeriod: 8712.03,
  overage: 9218.27,
  pricingUnitId: "<id>",
  currentPeriodStart: new Date("2025-06-15T11:35:12.121Z"),
  currentPeriodEnd: null,
};
```

