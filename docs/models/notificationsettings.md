# NotificationSettings

## Example Usage

```typescript
import { NotificationSettings } from "@paygentic/sdk/models";

let value: NotificationSettings = {
  invoiceIssued: false,
  invoicePaid: false,
  renewalReminder: true,
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `invoiceIssued`                                           | *boolean*                                                 | :heavy_check_mark:                                        | Whether to send invoice issued emails to this customer.   |
| `invoicePaid`                                             | *boolean*                                                 | :heavy_check_mark:                                        | Whether to send invoice paid emails to this customer.     |
| `renewalReminder`                                         | *boolean*                                                 | :heavy_check_mark:                                        | Whether to send renewal reminder emails to this customer. |