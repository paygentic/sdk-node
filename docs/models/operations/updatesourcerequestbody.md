# UpdateSourceRequestBody

## Example Usage

```typescript
import { UpdateSourceRequestBody } from "@paygentic/sdk/models/operations";

let value: UpdateSourceRequestBody = {};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `config`                                                                                       | Record<string, *any*>                                                                          | :heavy_minus_sign:                                                                             | Configuration specific to the source type                                                      |
| `description`                                                                                  | *string*                                                                                       | :heavy_minus_sign:                                                                             | Description of the source                                                                      |
| `enabled`                                                                                      | *boolean*                                                                                      | :heavy_minus_sign:                                                                             | Whether the source is enabled                                                                  |
| `metadata`                                                                                     | Record<string, *any*>                                                                          | :heavy_minus_sign:                                                                             | Metadata for the source                                                                        |
| `name`                                                                                         | *string*                                                                                       | :heavy_minus_sign:                                                                             | Display name for the source                                                                    |
| `processingMode`                                                                               | [operations.UpdateSourceProcessingMode](../../models/operations/updatesourceprocessingmode.md) | :heavy_minus_sign:                                                                             | How events are processed - automatic (immediate) or manual (requires approval)                 |