# Refund

Refund information for the usage event when it has been refunded. This object is populated by the server and returned in GET and PATCH responses. It cannot be set directly in request bodies.

## Example Usage

```typescript
import { Refund } from "@paygentic/sdk/models";

let value: Refund = {};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `reason`                                                                                                               | *string*                                                                                                               | :heavy_minus_sign:                                                                                                     | Reason for the refund. Sample values: 'Customer request', 'Billing error', 'Service credit', 'System error correction' |
| `refundedAt`                                                                                                           | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                          | :heavy_minus_sign:                                                                                                     | Timestamp when the usage event was refunded                                                                            |