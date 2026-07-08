# BillingVersion

Billing engine version. Only 1 (Standard, line-item billing with metered usage support) is accepted for new plans; omitting the field defaults to 1. 0 (Legacy, fee-schedule billing) is rejected — it exists only on plans created before this restriction.

## Example Usage

```typescript
import { BillingVersion } from "@paygentic/sdk/models/operations";

let value: BillingVersion = 1;
```

## Values

```typescript
0 | 1
```