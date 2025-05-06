---
tags:
  - Entra
---
- **Security Groups:** Designed to manage member permissions for resource access, like admin privs for specific resources for members of a group.
- **Microsoft 365 Group:** Shared resource for MS365 collaboration - like teams, outlook, SharePoint, etc. For instance, a "Finance" group can provide its members with a shared mailbox, document library, and OneNote notebook, enhancing team productivity.
- **Different assignment types:**
	- **Assigned** - Added manually to a group by an admin.
	- **Dynamic** - Added dynamically via a rule.
	- **Dynamic Device Groups** - Dynamic device groups apply only to security groups and function in a similar way as dynamic user groups, but they rely on device attributes. For example, you could set a rule to automatically include all devices running a specific operating system, enabling targeted software updates.


### Creating a Dynamic User Group

Dynamic user groups update automatically based on your defined criteria:

1. In Microsoft Entra ID, select Groups and click on "New Group."
    
2. Name the group (for example, "Avengers") and choose "Dynamic User" as the membership type.
    
3. Enter a dynamic query to define membership criteria. For example, to include users from the "Avengers" department, use:
    
    ```
    (user.department -eq "Avengers")
    ```
    
    To further refine the criteria (e.g., including only users in the US), modify the query as follows:
    
    ```
    (user.department -eq "Avengers") and (user.usageLocation -eq "US")
    ```
    
4. Save the rule. The system will automatically add users who meet the criteria and adjust membership if user attributes change.
    
5. Use the "Validate Rules" option to troubleshoot dynamic membership issues. For example, if a user like Gamora is missing from the "Avengers" group, the tool can help highlight that, despite matching one condition (e.g., usage location), the department attribute does not match.
    

### Creating a Dynamic Device Group

Dynamic device groups, available exclusively for security groups, rely on device properties (such as operating system or vendor):

1. Create a new group in Microsoft Entra ID, selecting "Dynamic Device" as the membership type.
2. Construct a dynamic query to include devices based on properties (for example, devices where the operating system is Windows).
3. Follow similar steps as for dynamic user groups, but base your query on device attributes.

Important

Ensure that device attribute data is accurate and up-to-date, as this directly affects dynamic group membership and subsequent policy applications.

