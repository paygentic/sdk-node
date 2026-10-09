# CustomerScope

## Example Usage

```typescript
import { CustomerScope } from "@paygentic/sdk/models";

let value: CustomerScope = {
  scope: "customer",
  customerId: "<id>",
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `scope`                          | *"customer"*                     | :heavy_check_mark:               | N/A                              |
| `customerId`                     | *string*                         | :heavy_check_mark:               | Unique identifier for a customer |