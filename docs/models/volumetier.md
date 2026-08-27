# VolumeTier

## Example Usage

```typescript
import { VolumeTier } from "@paygentic/sdk/models";

let value: VolumeTier = {
  upTo: "<value>",
  unitPrice: "<value>",
};
```

## Fields

| Field                                                                                                                                                                                         | Type                                                                                                                                                                                          | Required                                                                                                                                                                                      | Description                                                                                                                                                                                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `upTo`                                                                                                                                                                                        | *string*                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                            | Inclusive upper bound of the band, as a decimal string. Null on the last band only, which carries the remainder. Sample values: '100' bounds the band at 100 units, null leaves the top open. |
| `unitPrice`                                                                                                                                                                                   | *string*                                                                                                                                                                                      | :heavy_check_mark:                                                                                                                                                                            | Per-unit cost inside this band, as a decimal string, capped at 6 decimal places. Sample values: '5' represents $5 per unit, '0.004' represents $0.004 per unit.                               |