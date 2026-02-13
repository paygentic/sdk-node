# ParametersT

## Example Usage

```typescript
import { ParametersT } from "@paygentic/sdk/models";

let value: ParametersT = {
  function: "linear",
  gradient: "<value>",
  max: "<value>",
  min: "<value>",
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `function`                                    | [models.FunctionT](../models/functiont.md)    | :heavy_check_mark:                            | Function used for volume pricing calculations |
| `gradient`                                    | *string*                                      | :heavy_check_mark:                            | Gradient for volume pricing calculations      |
| `max`                                         | *string*                                      | :heavy_check_mark:                            | Maximum value for volume pricing              |
| `min`                                         | *string*                                      | :heavy_check_mark:                            | Minimum value for volume pricing              |