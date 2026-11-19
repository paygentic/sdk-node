# UpdateSubscriptionProposalRequest

## Example Usage

```typescript
import { UpdateSubscriptionProposalRequest } from "@paygentic/sdk/models/operations";

let value: UpdateSubscriptionProposalRequest = {
  id: "<id>",
  requestBody: {
    adjustments: [
      {
        type: "maximumQuantity",
        maximumQuantity: "<value>",
        targetPriceIds: [
          "<value 1>",
          "<value 2>",
        ],
        effectiveFrom: new Date("2025-07-12T04:11:53.725Z"),
      },
    ],
  },
};
```

## Fields

| Field                                                                                                                | Type                                                                                                                 | Required                                                                                                             | Description                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                 | *string*                                                                                                             | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |
| `requestBody`                                                                                                        | [operations.UpdateSubscriptionProposalRequestBody](../../models/operations/updatesubscriptionproposalrequestbody.md) | :heavy_check_mark:                                                                                                   | N/A                                                                                                                  |