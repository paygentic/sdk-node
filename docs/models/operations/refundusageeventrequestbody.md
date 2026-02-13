# RefundUsageEventRequestBody

## Example Usage

```typescript
import { RefundUsageEventRequestBody } from "@paygentic/sdk/models/operations";

let value: RefundUsageEventRequestBody = {
  refunded: false,
};
```

## Fields

| Field                                                                                                                           | Type                                                                                                                            | Required                                                                                                                        | Description                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| `refunded`                                                                                                                      | *boolean*                                                                                                                       | :heavy_check_mark:                                                                                                              | Set to true to mark the usage event as refunded. Once refunded, the event cannot be un-refunded.                                |
| `reason`                                                                                                                        | *string*                                                                                                                        | :heavy_minus_sign:                                                                                                              | Optional reason for the refund. Sample values: 'Customer request', 'Billing error', 'Service credit', 'System error correction' |