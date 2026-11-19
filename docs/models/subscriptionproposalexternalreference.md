# SubscriptionProposalExternalReference

The record in another system, such as a CRM deal, that the proposal comes from. A create naming a record that already has a proposal acts on that proposal, as the create operation describes.

## Example Usage

```typescript
import { SubscriptionProposalExternalReference } from "@paygentic/sdk/models";

let value: SubscriptionProposalExternalReference = {
  provider: "<value>",
  externalId: "<id>",
};
```

## Fields

| Field                                                                                                                             | Type                                                                                                                              | Required                                                                                                                          | Description                                                                                                                       |
| --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `provider`                                                                                                                        | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | Lowercase snake_case provider identifier (e.g. `salesforce`, `netsuite`)                                                          |
| `externalId`                                                                                                                      | *string*                                                                                                                          | :heavy_check_mark:                                                                                                                | Optional external identifier for cross-referencing with external systems. Alphanumeric characters, hyphens, and underscores only. |