# GetProfitabilityBucketWidth

Time bucket granularity for the per-customer revenue trend. When omitted, the server picks a reasonable bucket from the window length.

## Example Usage

```typescript
import { GetProfitabilityBucketWidth } from "@paygentic/sdk/models/operations";

let value: GetProfitabilityBucketWidth = "hour";
```

## Values

```typescript
"hour" | "day" | "week"
```