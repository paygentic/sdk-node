# ListPlanVersionsRequest

## Example Usage

```typescript
import { ListPlanVersionsRequest } from "@paygentic/sdk/models/operations";

let value: ListPlanVersionsRequest = {
  id: "<id>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `id`                                 | *string*                             | :heavy_check_mark:                   | N/A                                  |
| `limit`                              | *number*                             | :heavy_minus_sign:                   | Maximum number of versions to return |
| `offset`                             | *number*                             | :heavy_minus_sign:                   | Number of versions to skip           |