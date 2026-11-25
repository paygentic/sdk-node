# CreatePricingUnitRequest

## Example Usage

```typescript
import { CreatePricingUnitRequest } from "@paygentic/sdk/models/operations";

let value: CreatePricingUnitRequest = {
  merchantId: "<id>",
  identifier: "<value>",
  displayName: "Marley_Bruen",
  shortName: "<value>",
  conversionRate: "<value>",
  currency: "Rwanda Franc",
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `identifier`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Programmatic identifier, a slug unique per merchant (e.g. `credits`).                         |
| `displayName`                                                                                 | *string*                                                                                      | :heavy_check_mark:                                                                            | Human-readable name shown in the UI.                                                          |
| `shortName`                                                                                   | *string*                                                                                      | :heavy_check_mark:                                                                            | Short label used on invoice lines (e.g. `credits`).                                           |
| `conversionRate`                                                                              | *string*                                                                                      | :heavy_check_mark:                                                                            | Default rate converting one credit to the invoicing currency ($/credit), as a decimal string. |
| `currency`                                                                                    | *string*                                                                                      | :heavy_check_mark:                                                                            | ISO 4217 currency code that `conversionRate` maps to (e.g. `USD`).                            |