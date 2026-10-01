# EditSubscriptionIntervalsRequest

## Example Usage

```typescript
import { EditSubscriptionIntervalsRequest } from "@paygentic/sdk/models/operations";

let value: EditSubscriptionIntervalsRequest = {
  id: "<id>",
  editSubscriptionIntervalsRequest: {
    add: [
      {
        priceKey: "<value>",
        unitPrice: null,
        baseQuantity: "<value>",
        billingCadence: "<value>",
        billingMode: "advance",
        startDate: new Date("2025-11-04T22:49:10.595Z"),
      },
    ],
  },
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `id`                                           | *string*                                       | :heavy_check_mark:                             | The subscription ID                            |
| `editSubscriptionIntervalsRequest`             | *models.EditSubscriptionIntervalsRequestUnion* | :heavy_check_mark:                             | N/A                                            |