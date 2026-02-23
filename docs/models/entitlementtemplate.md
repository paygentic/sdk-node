# EntitlementTemplate

Template for the entitlement. Boolean for simple on/off features, static for features with configuration, metered for usage-based features.


## Supported Types

### `models.EntitlementTemplateBoolean`

```typescript
const value: models.EntitlementTemplateBoolean = {
  type: "boolean",
};
```

### `models.EntitlementTemplateStatic`

```typescript
const value: models.EntitlementTemplateStatic = {
  type: "static",
  config: {},
};
```

### `models.EntitlementTemplateMetered`

```typescript
const value: models.EntitlementTemplateMetered = {
  type: "metered",
  usagePeriod: {
    interval: "<value>",
  },
};
```

