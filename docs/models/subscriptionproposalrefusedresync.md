# SubscriptionProposalRefusedResync

The CRM's latest re-sync of this proposal that was refused, so a reviewer can see what the CRM asked for. A later send that applies or matches `requested`, an amend after which `current` holds every value it changed, and a reject clear it. A send that repeats it changes nothing.

## Example Usage

```typescript
import { SubscriptionProposalRefusedResync } from "@paygentic/sdk/models";

let value: SubscriptionProposalRefusedResync = {
  receivedAt: new Date("2026-11-17T14:55:25.422Z"),
  code: "SUBSCRIPTION_PROPOSAL_RESYNC_CONFLICT",
  fields: [],
  values: {
    customerId: "<id>",
    name: "<value>",
    planId: "<id>",
    startedAt: new Date("2025-06-24T21:11:03.224Z"),
    adjustments: [
      {
        type: "maximumQuantity",
        maximumQuantity: "<value>",
        targetPriceIds: [],
        effectiveFrom: new Date("2024-04-27T21:00:10.696Z"),
      },
    ],
  },
  credentialId: "<id>",
};
```

## Fields

| Field                                                                                                                                                                                    | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `receivedAt`                                                                                                                                                                             | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                            | :heavy_check_mark:                                                                                                                                                                       | When the refused values arrived.                                                                                                                                                         |
| `code`                                                                                                                                                                                   | [models.Code](../models/code.md)                                                                                                                                                         | :heavy_check_mark:                                                                                                                                                                       | The code of the 409 the send answered.                                                                                                                                                   |
| `fields`                                                                                                                                                                                 | *string*[]                                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                       | The fields that conflict with an amendment, or on an approved proposal the fields the CRM changed.                                                                                       |
| `values`                                                                                                                                                                                 | [models.SubscriptionProposalValues](../models/subscriptionproposalvalues.md)                                                                                                             | :heavy_check_mark:                                                                                                                                                                       | The values of a subscription proposal: the fields of `POST /v0/subscriptionProposals` without `externalReference`, each as that request takes it. A field the client left out is absent. |
| `credentialId`                                                                                                                                                                           | *string*                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                       | The key or OAuth client that sent them; null for a session.                                                                                                                              |