# SubscriptionProposalRevision

One set of values the client sent for a proposal. A revision never changes.

## Example Usage

```typescript
import { SubscriptionProposalRevision } from "@paygentic/sdk/models";

let value: SubscriptionProposalRevision = {
  id: "<id>",
  version: 820379,
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
  createdAt: new Date("2025-07-01T04:47:09.068Z"),
  createdByCredentialId: "<id>",
};
```

## Fields

| Field                                                                                                                                                                                    | Type                                                                                                                                                                                     | Required                                                                                                                                                                                 | Description                                                                                                                                                                              |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                                                                                     | *string*                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                       | N/A                                                                                                                                                                                      |
| `version`                                                                                                                                                                                | *number*                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                       | 1 for the values the proposal was created with, then one more for each set sent after.                                                                                                   |
| `values`                                                                                                                                                                                 | [models.SubscriptionProposalValues](../models/subscriptionproposalvalues.md)                                                                                                             | :heavy_check_mark:                                                                                                                                                                       | The values of a subscription proposal: the fields of `POST /v0/subscriptionProposals` without `externalReference`, each as that request takes it. A field the client left out is absent. |
| `createdAt`                                                                                                                                                                              | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                                            | :heavy_check_mark:                                                                                                                                                                       | N/A                                                                                                                                                                                      |
| `createdByCredentialId`                                                                                                                                                                  | *string*                                                                                                                                                                                 | :heavy_check_mark:                                                                                                                                                                       | The API key or OAuth client that sent the values; null for a dashboard session.                                                                                                          |