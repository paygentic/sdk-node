# SubscriptionProposalDecider

Who decided a proposal.

## Example Usage

```typescript
import { SubscriptionProposalDecider } from "@paygentic/sdk/models";

let value: SubscriptionProposalDecider = {
  type: "apiKey",
  name: "<value>",
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `type`                                                                                 | [models.SubscriptionProposalDeciderType](../models/subscriptionproposaldecidertype.md) | :heavy_check_mark:                                                                     | `user` for a member of the merchant, `apiKey` for an API key. Open set.                |
| `name`                                                                                 | *string*                                                                               | :heavy_check_mark:                                                                     | A user's first and last name, or their email when both are blank; an API key's name.   |