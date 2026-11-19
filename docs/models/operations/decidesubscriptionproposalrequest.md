# DecideSubscriptionProposalRequest

## Example Usage

```typescript
import { DecideSubscriptionProposalRequest } from "@paygentic/sdk/models/operations";

let value: DecideSubscriptionProposalRequest = {
  id: "<id>",
  subscriptionProposalDecision: {
    decision: "reject",
    basedOnHash: "<value>",
  },
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `id`                                                                                | *string*                                                                            | :heavy_check_mark:                                                                  | The subscription proposal ID                                                        |
| `subscriptionProposalDecision`                                                      | [models.SubscriptionProposalDecision](../../models/subscriptionproposaldecision.md) | :heavy_check_mark:                                                                  | N/A                                                                                 |