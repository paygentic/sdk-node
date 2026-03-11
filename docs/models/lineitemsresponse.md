# LineItemsResponse

## Example Usage

```typescript
import { LineItemsResponse } from "@paygentic/sdk/models";

let value: LineItemsResponse = {
  object: "list",
  data: [],
  totalCount: 46840,
  summary: {
    feeSubtotal: "<value>",
    meteredEstimatedSubtotal: "<value>",
    currency: "Djibouti Franc",
  },
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `object`                                                               | [models.LineItemsResponseObject](../models/lineitemsresponseobject.md) | :heavy_check_mark:                                                     | The object type                                                        |
| `data`                                                                 | [models.LineItem](../models/lineitem.md)[]                             | :heavy_check_mark:                                                     | Array of line items                                                    |
| `totalCount`                                                           | *number*                                                               | :heavy_check_mark:                                                     | Total number of matching line items                                    |
| `summary`                                                              | [models.LineItemsSummary](../models/lineitemssummary.md)               | :heavy_check_mark:                                                     | N/A                                                                    |