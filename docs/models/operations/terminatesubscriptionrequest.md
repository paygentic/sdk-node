# TerminateSubscriptionRequest

## Example Usage

```typescript
import { TerminateSubscriptionRequest } from "@paygentic/sdk/models/operations";

let value: TerminateSubscriptionRequest = {
  id: "<id>",
  requestBody: {
    reason: "<value>",
  },
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                       | *string*                                                                                                   | :heavy_check_mark:                                                                                         | The subscription ID                                                                                        |
| `requestBody`                                                                                              | [operations.TerminateSubscriptionRequestBody](../../models/operations/terminatesubscriptionrequestbody.md) | :heavy_check_mark:                                                                                         | N/A                                                                                                        |