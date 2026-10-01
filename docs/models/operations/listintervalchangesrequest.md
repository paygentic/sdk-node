# ListIntervalChangesRequest

## Example Usage

```typescript
import { ListIntervalChangesRequest } from "@paygentic/sdk/models/operations";

let value: ListIntervalChangesRequest = {};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `limit`                                                                                       | *string*                                                                                      | :heavy_minus_sign:                                                                            | Number of interval changes to return                                                          |
| `offset`                                                                                      | *string*                                                                                      | :heavy_minus_sign:                                                                            | Number of interval changes to skip                                                            |
| `from`                                                                                        | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Only return changes recorded at or after this time                                            |
| `to`                                                                                          | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_minus_sign:                                                                            | Only return changes recorded before this time                                                 |
| `changeReason`                                                                                | [models.ChangeReason](../../models/changereason.md)                                           | :heavy_minus_sign:                                                                            | Only return changes with this reason.                                                         |