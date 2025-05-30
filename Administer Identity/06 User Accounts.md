---
tags:
  - Entra
---
- The foundational element of Entra ID are user accounts.
- These accounts are the digital passcode to a world of resources and services in your org, not just a username and password.
- The cornerstone of authn and authz, ensuring each user has a unique digital ID in the workspace.
- To access resources and apps securely, each user must have an account.
- Each acc can have optional props like address, department, etc.
- Helps streamline comms and workflows. 
- Admins can access all user acc in the Entra portal under **Users > All users.**
- We can also perform **bulk operations** for CRUD stuff on user accouns.
- Multiple account types:
  - **Cloud identity:** Exists purely in the cloud, no on premise AD. Good for orgs that are only in the cloud. Can be your own or external Entra ID.
  - **Guest accounts:** Allow people from outside the orgs access to resources (contractors or whoever else needs guest access to collab). Could be any other account, like gmail or something.  **If a user belongs to another company with its own Entra ID, they are treated as a cloud identity; however, if that user does not have an Entra ID, the account is considered a guest account.**
  - **Directory Synced Users:** Synced from on premise AD to the cloud with Microsoft Entra ID Connect. Creates a unified identity framework from OP to the cloud.