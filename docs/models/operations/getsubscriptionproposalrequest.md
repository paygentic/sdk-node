# GetSubscriptionProposalRequest

## Example Usage

```typescript
import { GetSubscriptionProposalRequest } from "@paygentic/sdk/models/operations";

let value: GetSubscriptionProposalRequest = {
  id: "<id>",
};
```

## Fields

| Field                                                  | Type                                                   | Required                                               | Description                                            |
| ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------ |
| `id`                                                   | *string*                                               | :heavy_check_mark:                                     | N/A                                                    |
| `expand`                                               | [operations.Expand](../../models/operations/expand.md) | :heavy_minus_sign:                                     | `revisions` adds the proposal's revisions.             |