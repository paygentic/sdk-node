# NotificationSettings

Notification preferences for this customer. Only provided fields are updated.

## Example Usage

```typescript
import { NotificationSettings } from "@paygentic/sdk/models/operations";

let value: NotificationSettings = {};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `invoiceIssued`                                           | *boolean*                                                 | :heavy_minus_sign:                                        | Whether to send invoice issued emails to this customer.   |
| `invoicePaid`                                             | *boolean*                                                 | :heavy_minus_sign:                                        | Whether to send invoice paid emails to this customer.     |
| `renewalReminder`                                         | *boolean*                                                 | :heavy_minus_sign:                                        | Whether to send renewal reminder emails to this customer. |