# TerminateSubscriptionRequestBody

## Example Usage

```typescript
import { TerminateSubscriptionRequestBody } from "@paygentic/sdk/models/operations";

let value: TerminateSubscriptionRequestBody = {
  reason: "<value>",
};
```

## Fields

| Field                                                                                                                                          | Type                                                                                                                                           | Required                                                                                                                                       | Description                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `reason`                                                                                                                                       | *string*                                                                                                                                       | :heavy_check_mark:                                                                                                                             | Cancellation explanation text. Sample values: 'Customer requested cancellation', 'Payment failure', 'Service migration', 'Contract expiration' |