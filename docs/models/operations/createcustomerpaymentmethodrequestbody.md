# CreateCustomerPaymentMethodRequestBody

## Example Usage

```typescript
import { CreateCustomerPaymentMethodRequestBody } from "@paygentic/sdk/models/operations";

let value: CreateCustomerPaymentMethodRequestBody = {};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `successRedirectUrl`                                                                                                   | *string*                                                                                                               | :heavy_minus_sign:                                                                                                     | URL the customer is redirected to on success. When the page is iframed, success is reported via `postMessage` instead. |
| `failureRedirectUrl`                                                                                                   | *string*                                                                                                               | :heavy_minus_sign:                                                                                                     | URL the customer is redirected to on failure. When the page is iframed, failure is reported via `postMessage` instead. |
| `metadata`                                                                                                             | Record<string, *any*>                                                                                                  | :heavy_minus_sign:                                                                                                     | Arbitrary key/value pairs to attach to the session.                                                                    |