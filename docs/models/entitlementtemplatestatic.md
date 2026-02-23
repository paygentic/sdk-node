# EntitlementTemplateStatic

## Example Usage

```typescript
import { EntitlementTemplateStatic } from "@paygentic/sdk/models";

let value: EntitlementTemplateStatic = {
  type: "static",
  config: {},
};
```

## Fields

| Field                                     | Type                                      | Required                                  | Description                               |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| `type`                                    | *"static"*                                | :heavy_check_mark:                        | N/A                                       |
| `config`                                  | Record<string, *any*>                     | :heavy_check_mark:                        | Configuration values for the entitlement. |