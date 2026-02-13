# Summary

Summary of batch processing results

## Example Usage

```typescript
import { Summary } from "@paygentic/sdk/models";

let value: Summary = {
  failed: 717063,
  successful: 399543,
  total: 950147,
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `failed`                                   | *number*                                   | :heavy_check_mark:                         | Number of events that failed to be created |
| `successful`                               | *number*                                   | :heavy_check_mark:                         | Number of successfully created events      |
| `total`                                    | *number*                                   | :heavy_check_mark:                         | Total number of events in the batch        |