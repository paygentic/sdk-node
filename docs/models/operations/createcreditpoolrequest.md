# CreateCreditPoolRequest

## Example Usage

```typescript
import { CreateCreditPoolRequest } from "@paygentic/sdk/models/operations";

let value: CreateCreditPoolRequest = {
  customerId: "<id>",
  pricingUnitId: "<id>",
};
```

## Fields

| Field                                | Type                                 | Required                             | Description                          |
| ------------------------------------ | ------------------------------------ | ------------------------------------ | ------------------------------------ |
| `customerId`                         | *string*                             | :heavy_check_mark:                   | Unique identifier for a customer     |
| `pricingUnitId`                      | *string*                             | :heavy_check_mark:                   | Unique identifier for a pricing unit |