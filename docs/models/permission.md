# Permission

A permission of the catalog: a resource read or write, or a sensitive action.

## Example Usage

```typescript
import { Permission } from "@paygentic/sdk/models";

let value: Permission = "subscriptions:update";
```

## Values

```typescript
"organization:read" | "members:read" | "profile:read" | "apiKeys:read" | "merchants:read" | "consumers:read" | "customers:read" | "plans:read" | "prices:read" | "products:read" | "features:read" | "fees:read" | "billableMetrics:read" | "items:read" | "pricingUnits:read" | "subscriptions:read" | "subscriptionAdjustments:read" | "discounts:read" | "grants:read" | "entitlements:read" | "creditPools:read" | "orders:read" | "billingSchedules:read" | "invoices:read" | "payments:read" | "paymentSessions:read" | "portalSessions:read" | "platformUsers:read" | "platformAdmin:read" | "organizationCreation:read" | "compliance:read" | "taxSettings:read" | "costs:read" | "paymentAccounts:read" | "payouts:read" | "externalAccounts:read" | "externalReferences:read" | "merchantIntegrations:read" | "webhooks:read" | "testClocks:read" | "approvals:read" | "sources:read" | "revenue:read" | "organization:write" | "members:write" | "profile:write" | "apiKeys:write" | "merchants:write" | "consumers:write" | "customers:write" | "plans:write" | "prices:write" | "products:write" | "features:write" | "fees:write" | "billableMetrics:write" | "items:write" | "pricingUnits:write" | "subscriptions:write" | "subscriptionAdjustments:write" | "discounts:write" | "grants:write" | "entitlements:write" | "creditPools:write" | "orders:write" | "billingSchedules:write" | "invoices:write" | "payments:write" | "paymentSessions:write" | "portalSessions:write" | "platformUsers:write" | "platformAdmin:write" | "organizationCreation:write" | "compliance:write" | "taxSettings:write" | "costs:write" | "paymentAccounts:write" | "payouts:write" | "externalAccounts:write" | "externalReferences:write" | "merchantIntegrations:write" | "webhooks:write" | "testClocks:write" | "approvals:write" | "sources:write" | "events:write" | "invoices:issue" | "invoices:void" | "payments:refund" | "organization:delete" | "ownership:transfer" | "subscriptions:terminate" | "subscriptions:terminateWithReason" | "subscriptions:reconcile" | "subscriptions:update" | "subscriptions:delete" | "subscriptions:taxExempt" | "subscriptions:autoApprove" | "organization:resetData"
```