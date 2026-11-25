# CreditPool

## Example Usage

```typescript
import { CreditPool } from "@paygentic/sdk/models";

let value: CreditPool = {
  id: "<id>",
  customerId: "<id>",
  pricingUnitId: "<id>",
  createdAt: new Date("2026-01-11T14:28:15.385Z"),
  updatedAt: new Date("2026-11-19T01:53:39.649Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `object`                                                                                      | [models.CreditPoolObject](../models/creditpoolobject.md)                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `customerId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a customer                                                              |
| `pricingUnitId`                                                                               | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a pricing unit                                                          |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |