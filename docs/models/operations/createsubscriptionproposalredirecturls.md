# CreateSubscriptionProposalRedirectUrls

Optional redirect URLs after payment completion or failure. If not provided, uses default platform behavior.

## Example Usage

```typescript
import { CreateSubscriptionProposalRedirectUrls } from "@paygentic/sdk/models/operations";

let value: CreateSubscriptionProposalRedirectUrls = {};
```

## Fields

| Field                                                                                                                                                                          | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `onSuccess`                                                                                                                                                                    | *string*                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                             | Redirect destination after successful payment. Sample values: 'https://app.example.com/success', 'https://dashboard.company.com/welcome', 'https://portal.startup.io/complete' |
| `onFailure`                                                                                                                                                                    | *string*                                                                                                                                                                       | :heavy_minus_sign:                                                                                                                                                             | Redirect destination after failed payment. Sample values: 'https://app.example.com/payment-failed', 'https://dashboard.company.com/retry', 'https://portal.startup.io/error'   |