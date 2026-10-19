# AccountFigure

A number of invoices and their total amount due, gross of tax.

## Example Usage

```typescript
import { AccountFigure } from "@paygentic/sdk/models";

let value: AccountFigure = {
  count: 206363,
  amount: "709.01",
};
```

## Fields

| Field                                                                                                                       | Type                                                                                                                        | Required                                                                                                                    | Description                                                                                                                 |
| --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- |
| `count`                                                                                                                     | *number*                                                                                                                    | :heavy_check_mark:                                                                                                          | Number of invoices with an amount due above zero. A credit invoice, or one whose amount due rounds to zero, is not counted. |
| `amount`                                                                                                                    | *string*                                                                                                                    | :heavy_check_mark:                                                                                                          | Total amount due in major units of the currency, in its decimal places                                                      |