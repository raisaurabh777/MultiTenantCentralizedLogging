## Multi-Tenant Centralized Logging Using Azure Lighthouse
- Service Provider: The tenant whose logs should be sent to a Central Log Analytics Workspace which is present in another tenant.
- Customer: The tenant where the Central Log Analytics Workspace exists.

For centralized logging to work, we need to create an offer from Service Provider Tenant and import it into the Customer Tenant. The offer allows the Service Provider Tenant have access to the Centralized Log Analytics in Customer Tenant.

The default Offer (JSON) file for onboarding a Service Provider Tenant to a Customer Tenant for Centralized Logging is named as "onboarding-serviceprovideroffer-to-customer.json".

To customize the onboarding process for individual tenant(s), the file "onboarding-serviceprovideroffer-to-customer.parameters.json" must be updated accordingly and imported within the Customer's Tenant i.e. where central log analytics is present. This action grants specified security group(s) from Service Provider tenant access to the central Log Analytics Workspace (LAW) in the Customer tenant.
