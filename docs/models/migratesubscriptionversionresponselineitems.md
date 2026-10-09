# MigrateSubscriptionVersionResponseLineItems

## Example Usage

```typescript
import { MigrateSubscriptionVersionResponseLineItems } from "@paygentic/sdk/models";

let value: MigrateSubscriptionVersionResponseLineItems = {
  syncFailed: true,
};
```

## Fields

| Field                                                                                                                                               | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `syncFailed`                                                                                                                                        | *boolean*                                                                                                                                           | :heavy_check_mark:                                                                                                                                  | True when the migration was saved but the line-item re-derive failed. The migration is not rolled back, and the re-derive is retried automatically. |