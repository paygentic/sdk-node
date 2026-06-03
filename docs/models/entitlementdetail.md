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
  productId: "<id>",
  subscriptionId: "<id>",
  status: "active",
  activeFrom: new Date("2025-01-21T21:06:13.346Z"),
  activeTo: new Date("2024-08-28T01:51:57.180Z"),
  hasAccess: true,
  metadata: {},
  config: {
    "key": "<value>",
    "key1": "<value>",
  },
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
  productId: "<id>",
  subscriptionId: "<id>",
  status: "expired",
  activeFrom: new Date("2024-02-25T20:41:20.667Z"),
  activeTo: new Date("2025-12-25T06:44:37.128Z"),
  hasAccess: true,
  metadata: {},
  config: {
    "key": "<value>",
  },
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
  productId: "<id>",
  subscriptionId: "<id>",
  status: "canceled",
  activeFrom: new Date("2024-12-07T17:10:23.685Z"),
  activeTo: new Date("2026-09-11T16:32:25.801Z"),
  hasAccess: false,
  metadata: {
    "key": "<value>",
    "key1": "<value>",
  },
  config: {
    "key": "<value>",
    "key1": "<value>",
    "key2": "<value>",
  },
  isSoftLimit: false,
  balance: 7018.52,
  usageInPeriod: 8437.34,
  overage: 2184.15,
  currentPeriodStart: new Date("2024-09-02T08:01:20.933Z"),
  currentPeriodEnd: null,
};
```

