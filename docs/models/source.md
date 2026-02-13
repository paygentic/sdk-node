# Source

## Example Usage

```typescript
import { Source } from "@paygentic/sdk/models";

let value: Source = {
  id: "<id>",
  object: "source",
  createdAt: new Date("2024-02-10T08:27:14.362Z"),
  enabled: true,
  merchantId: "<id>",
  name: "<value>",
  planId: "<id>",
  processingMode: "automatic",
  type: "stripe_revenue",
  updatedAt: new Date("2026-12-11T10:45:12.815Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `id`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a source                                                                |
| `object`                                                                                      | [models.SourceObject](../models/sourceobject.md)                                              | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `config`                                                                                      | Record<string, *any*>                                                                         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `createdAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `description`                                                                                 | *string*                                                                                      | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `enabled`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `merchantId`                                                                                  | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for an organization                                                         |
| `metadata`                                                                                    | Record<string, *any*>                                                                         | :heavy_minus_sign:                                                                            | N/A                                                                                           |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `planId`                                                                                      | *string*                                                                                      | :heavy_check_mark:                                                                            | Unique identifier for a plan                                                                  |
| `processingMode`                                                                              | [models.ProcessingMode](../models/processingmode.md)                                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `type`                                                                                        | [models.SourceType](../models/sourcetype.md)                                                  | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |