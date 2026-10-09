# RetryPaymentResponseError

The result of a payment retry. Every response status of the retry operation that is not an error envelope uses this shape.

## Example Usage

```typescript
import { RetryPaymentResponseError } from "@paygentic/sdk/models/errors";

// No examples available for this model
```

## Fields

| Field                                                                                                          | Type                                                                                                           | Required                                                                                                       | Description                                                                                                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| `object`                                                                                                       | [models.RetryPaymentResponseObject](../../models/retrypaymentresponseobject.md)                                | :heavy_check_mark:                                                                                             | The object type                                                                                                |
| `success`                                                                                                      | *boolean*                                                                                                      | :heavy_check_mark:                                                                                             | True only when the charge succeeded or no amount is unpaid. The response status is 200 only when this is true. |
| `invoiceId`                                                                                                    | *string*                                                                                                       | :heavy_check_mark:                                                                                             | The invoice ID                                                                                                 |
| `paymentIntentId`                                                                                              | *string*                                                                                                       | :heavy_minus_sign:                                                                                             | The provider's payment reference for the charge, when the provider has one.                                    |
| `error`                                                                                                        | [models.RetryPaymentError](../../models/retrypaymenterror.md)                                                  | :heavy_minus_sign:                                                                                             | Why a payment retry did not collect the money.                                                                 |