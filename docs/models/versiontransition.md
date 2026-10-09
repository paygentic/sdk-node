# VersionTransition

When a move to a new plan version takes effect for this plan's subscriptions. `end_of_current_period` (the default) moves everything at the end of the current billing period. `immediate` changes entitlements at the move, in-arrears prices for the whole current period, and in-advance prices from the next period. Neither prorates.

## Example Usage

```typescript
import { VersionTransition } from "@paygentic/sdk/models";

let value: VersionTransition = {
  effectiveDate: "immediate",
  proration: "none",
};
```

## Fields

| Field                                                      | Type                                                       | Required                                                   | Description                                                |
| ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------- |
| `effectiveDate`                                            | [models.EffectiveDate](../models/effectivedate.md)         | :heavy_check_mark:                                         | When the move takes effect.                                |
| `proration`                                                | [models.Proration](../models/proration.md)                 | :heavy_check_mark:                                         | How the current period is split. Only `none` is supported. |