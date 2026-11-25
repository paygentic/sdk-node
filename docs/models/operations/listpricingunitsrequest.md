# ListPricingUnitsRequest

## Example Usage

```typescript
import { ListPricingUnitsRequest } from "@paygentic/sdk/models/operations";

let value: ListPricingUnitsRequest = {};
```

## Fields

| Field                                            | Type                                             | Required                                         | Description                                      |
| ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ | ------------------------------------------------ |
| `merchantId`                                     | *string*                                         | :heavy_minus_sign:                               | Filter pricing units by merchant organization id |
| `limit`                                          | *number*                                         | :heavy_minus_sign:                               | Maximum pricing units to return                  |
| `offset`                                         | *number*                                         | :heavy_minus_sign:                               | Zero-based offset for pagination                 |