# CreateItemRequest

## Example Usage

```typescript
import { CreateItemRequest } from "@paygentic/sdk/models/operations";

let value: CreateItemRequest = {
  merchantId: "<id>",
  name: "<value>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `merchantId`                         | *string*                             | :heavy_check_mark:                   | N/A                                  |
| `name`                               | *string*                             | :heavy_check_mark:                   | Canonical sellable name for the Item |
| `metadata`                           | Record<string, *any*>                | :heavy_minus_sign:                   | Optional key-value metadata          |