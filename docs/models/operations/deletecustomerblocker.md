# DeleteCustomerBlocker

## Example Usage

```typescript
import { DeleteCustomerBlocker } from "@paygentic/sdk/models/operations";

let value: DeleteCustomerBlocker = {
  type: "entitlements",
  count: 948917,
  items: [
    {},
  ],
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `type`                                                                         | [operations.DeleteCustomerType](../../models/operations/deletecustomertype.md) | :heavy_check_mark:                                                             | N/A                                                                            |
| `count`                                                                        | *number*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |
| `items`                                                                        | [operations.Item](../../models/operations/item.md)[]                           | :heavy_check_mark:                                                             | N/A                                                                            |