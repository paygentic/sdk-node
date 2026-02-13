# UpdateSourceRequest

## Example Usage

```typescript
import { UpdateSourceRequest } from "@paygentic/sdk/models/operations";

let value: UpdateSourceRequest = {
  id: "<id>",
  requestBody: {},
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `id`                                                                                     | *string*                                                                                 | :heavy_check_mark:                                                                       | The unique identifier of the source                                                      |
| `requestBody`                                                                            | [operations.UpdateSourceRequestBody](../../models/operations/updatesourcerequestbody.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |