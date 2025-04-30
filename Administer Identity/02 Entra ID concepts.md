- **Identity** is any object that can be authenticated.
	- **User:** Represents an individual with access to services.
	- **Group:** A collection of users often managed together.
	- **Managed Identity:** The identity associated with a service in Azure (such as a virtual machine or app service) that enables secure access to other services.
	- **Service Principal:** Similar to on-premises service accounts, these are used for automated tasks or to execute processes on behalf of a user.
- **Account** is when we assign data attributes to an identity. A user might have multiple attributes, like location, department, etc.
- **Microsoft Entra ID Account** is an account created in Entra ID or another Microsoft cloud service.
  Can be a work/school account, or a personal MS account for example.
  Both types of accounts ensure secure and efficient access to Microsoft services while using a unified identity management system.
- **Microsoft Entra ID or Tenant or Directory**. This is a **dedicated** instance of MS Entra ID that is automatically generated during the sign up process for any MS cloud service subscription. When you create an Azure account, you create a tenant automatically, an all associated subscriptions are mapped to this tenant. 


## Key Takeaways

- **Identity:** The foundational element used for authentication (including users, groups, managed identities, and service principals).
- **Account:** An identity enriched with detailed data attributes.
- **Microsoft Entra ID Account:** An account provisioned via Microsoft Entra ID that supports both work/school and personal use cases.
- **Tenant/Directory:** A dedicated instance of Microsoft Entra ID that organizes your subscriptions and resources.