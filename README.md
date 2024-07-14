# SentinelRBAC
A small project in search of least permissions for Azure custom roles on Microsoft Sentinel

My personal opinion is that you **should not** use custom roles and use Built-In Roles provided bu Azure. Custom roles if not ptoperly scoped may lead to inadvertent over permissions in role design. That said I recommend temporary during the deployment phase of Microsoft Sentinel granting the following Built-In Azure roles during the deployment and configuration:

Deploy a Sentinel Resource Group 'rgSentinel'

On scope \subscription\{SubId}\ResourceGroup\reSentinel

[Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/general#contributor)

On scope \subscription\{SubId}

[Monitoring Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/monitor#monitoring-contributor)

On scope \rootMG

[Resource Policy Contributor](https://learn.microsoft.com/en-us/azure/role-based-access-control/built-in-roles/management-and-governance#resource-policy-contributor)

With all that being said I am still curious and the following repository will host custom roles defined through a series of blogs at [SwiftSolves Substack](https://swiftsolves.substack.com/)
