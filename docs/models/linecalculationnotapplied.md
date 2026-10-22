# LineCalculationNotApplied

A rule in force for the line that did not change it.

## Example Usage

```typescript
import { LineCalculationNotApplied } from "@paygentic/sdk/models";

let value: LineCalculationNotApplied = {
  source: "<value>",
  reason: "<value>",
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `source`                                                                    | *string*                                                                    | :heavy_check_mark:                                                          | The key of the rule's source in `sources`.                                  |
| `reason`                                                                    | *string*                                                                    | :heavy_check_mark:                                                          | Why the rule did not change the line, for example `within` or `notBinding`. |