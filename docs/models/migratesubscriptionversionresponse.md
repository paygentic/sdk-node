# MigrateSubscriptionVersionResponse

## Example Usage

```typescript
import { MigrateSubscriptionVersionResponse } from "@paygentic/sdk/models";

let value: MigrateSubscriptionVersionResponse = {
  subscription: {
    id: "<id>",
    object: "subscription",
    merchantId: "<id>",
    createdAt: new Date("2024-02-14T03:12:08.201Z"),
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    versionPolicy: "floating",
    startedAt: new Date("2026-04-30T13:00:19.545Z"),
    elapsedPeriodBilling: "none",
    billingStartsAt: new Date("2026-06-29T14:20:44.225Z"),
    billingAnchor: new Date("2026-01-07T03:05:51.257Z"),
    billingCadence: "P1M",
    status: "active",
    updatedAt: new Date("2025-03-15T00:26:54.750Z"),
    paymentTermDays: 697662,
  },
  migration: {
    fromVersionNumber: 312927,
    toVersionNumber: 851868,
    effectiveAt: new Date("2024-08-09T03:02:01.172Z"),
    entitlementsEffectiveAt: new Date("2025-04-26T17:29:47.230Z"),
    changed: true,
  },
  lineItems: {
    syncFailed: true,
  },
};
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `subscription`                                                                                                 | [models.Subscription](../models/subscription.md)                                                               | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `migration`                                                                                                    | [models.Migration](../models/migration.md)                                                                     | :heavy_check_mark:                                                                                             | N/A                                                                                                            |
| `lineItems`                                                                                                    | [models.MigrateSubscriptionVersionResponseLineItems](../models/migratesubscriptionversionresponselineitems.md) | :heavy_check_mark:                                                                                             | N/A                                                                                                            |