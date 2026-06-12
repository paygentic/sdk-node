# UpdateItemRequest

## Example Usage

```typescript
import { UpdateItemRequest } from "@paygentic/sdk/models/operations";

let value: UpdateItemRequest = {
  id: "<id>",
  requestBody: {},
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `id`                                                                                 | *string*                                                                             | :heavy_check_mark:                                                                   | The unique identifier of the item                                                    |
| `requestBody`                                                                        | [operations.UpdateItemRequestBody](../../models/operations/updateitemrequestbody.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |