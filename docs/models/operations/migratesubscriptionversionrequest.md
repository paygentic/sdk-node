# MigrateSubscriptionVersionRequest

## Example Usage

```typescript
import { MigrateSubscriptionVersionRequest } from "@paygentic/sdk/models/operations";

let value: MigrateSubscriptionVersionRequest = {
  id: "<id>",
  migrateSubscriptionVersionRequest: {
    targetVersionNumber: 792531,
  },
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | The subscription ID                                                                           |
| `migrateSubscriptionVersionRequest`                                                           | [models.MigrateSubscriptionVersionRequest](../../models/migratesubscriptionversionrequest.md) | :heavy_check_mark:                                                                            | N/A                                                                                           |