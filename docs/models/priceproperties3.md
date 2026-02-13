# PriceProperties3

Volume pricing model

## Example Usage

```typescript
import { PriceProperties3 } from "@paygentic/sdk/models";

let value: PriceProperties3 = {
  default: "<value>",
  parameters: {
    function: "linear",
    gradient: "<value>",
    max: "<value>",
    min: "<value>",
  },
};
```

## Fields

| Field                                          | Type                                           | Required                                       | Description                                    |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| `default`                                      | *string*                                       | :heavy_check_mark:                             | Default value for volume pricing               |
| `parameters`                                   | [models.ParametersT](../models/parameterst.md) | :heavy_check_mark:                             | N/A                                            |