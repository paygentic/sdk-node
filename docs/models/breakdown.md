# Breakdown

Breakdown of payment amount

## Example Usage

```typescript
import { Breakdown } from "@paygentic/sdk/models";

let value: Breakdown = {
  upfrontCharges: "<value>",
  walletCharge: "<value>",
};
```

## Fields

| Field                                                                                                                                      | Type                                                                                                                                       | Required                                                                                                                                   | Description                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| `upfrontCharges`                                                                                                                           | *string*                                                                                                                                   | :heavy_check_mark:                                                                                                                         | One-time flat fee charges in decimal dollar format. Sample values: '50.00' equals $50.00 setup fee, '100.00' equals $100.00 activation fee |
| `walletCharge`                                                                                                                             | *string*                                                                                                                                   | :heavy_check_mark:                                                                                                                         | Wallet charge amount in decimal dollar format.                                                                                             |