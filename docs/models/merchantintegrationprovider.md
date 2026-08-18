# MerchantIntegrationProvider

External provider a merchant can connect at the tenant level. `netsuite` and `accountsiq` are returned on reads wherever a connection exists, but connecting them is accepted only in local and development environments; elsewhere the connect request is refused with 404.

## Example Usage

```typescript
import { MerchantIntegrationProvider } from "@paygentic/sdk/models";

let value: MerchantIntegrationProvider = "salesforce";
```

## Values

```typescript
"salesforce" | "netsuite" | "accountsiq"
```