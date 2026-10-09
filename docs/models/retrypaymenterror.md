# RetryPaymentError

Why a payment retry did not collect the money.

## Example Usage

```typescript
import { RetryPaymentError } from "@paygentic/sdk/models";

let value: RetryPaymentError = {
  message: "<value>",
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `message`                                                              | *string*                                                               | :heavy_check_mark:                                                     | Human-readable message. Do not parse it; use `code`.                   |
| `type`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | Error category, for example `card_error` or `processing`.              |
| `code`                                                                 | *string*                                                               | :heavy_minus_sign:                                                     | Machine-readable reason. See the operation description for the values. |
| `declineCode`                                                          | *string*                                                               | :heavy_minus_sign:                                                     | The card decline code from the provider, when one is available.        |