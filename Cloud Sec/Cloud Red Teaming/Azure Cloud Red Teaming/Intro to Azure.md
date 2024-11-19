- Is a Cloud computing service created by Microsoft for building,testing, deploying and managing applications and services though Microsoft-managed data centers.
- Azure is divided into 3 components:
![[azure.png]]
## 1. Azure AD/ Entra ID 
- Microsoft's enterprise cloud based identity access management solution providing Identity as a service **IdAAs**
- Backbone of the [[#3. Office 365 | Office 365 System]] and can sync with on-prem Active Directory and provide  authentication to other cloud based systems via OAuth.
- Can connect to __Active Directory, on-premises applications, external identities(okta) and cloud services(office 365)__

### 1.1 Entra ID Objects
- Each Azure AD object has a unique ID associated with it called Object id, examples of these objects:
	- Users
	- Groups
	- Devices
	- Applications 
	
- These can be further split as seen in the image below:
![[Objects.jpeg]]
>[!info]
>Enterprise applications use Service Principles to access the cloud service from third party applications i.e Terraform and the CLI

### 1.2 Entra ID Directory Roles

-  Set of predefined roles that grant permissions to perform specific tasks within Azure AD Tenant.
- There are two types of roles in Entra ID
	1. Built-in Directory Roles
		- Global Administrator - Perform any task on Entra ID
		- Application Administrator - Create applications and credentials
		- User Administrator - User and password creation.
	2. Custom Directory Role - Custom created rules and permissions.

> [!tip] Microsoft Graph API endpoint
> To Perform any operations on Azure AD/Entra ID we use the below API endpoint
> {HTTP method} https://graph.microsoft.com/{version}/{resource}?{query-parameters}

## 2. Azure Resource Manager(ARM):

> [!info]
> ARM Provides the below services: 
> 1. Infrastructure as a Service **IAAS**
> 2. Platform as a Service **PAAS**
> 3. Software as a service **SAAS**

- Manages all resources that are created in Azure.
- Native platform for **Infrastructure as Code** in Azure enabling centralized management,deployment and security of Azure resources.
- Manages access control via Role Based Access Control (RBAC)

> [!note] 
> Azure Resource Manager Resource Hierarchy
> ![[resource.jpeg]]

>[!tip]
>A unique Tenant ID is generated for your domain.
>Management group manages subscriptions which are used for billing.
>Each subscription has a resource group which is a container for your resources.

### 2.1 Role Based Access Management(RBAC)

- Authorization system built into ARM which allows for fine-grained access management to Azure resources.
- To perform **role assignment** on Azure we need to define the following:
	-  [[#2.2 Service Principal | Security principal]] - this is the identity ie **[[#1.1 Entra ID Objects | Entra ID Objects]]**
	- [[#2.3 Scope | Scope]]
	- [[#2.4 Roles | Role definition]] - set of permissions


### 2.2 Security Principal

- Object that represents a user, group, service principal or Managed Identity(User or system assigned) that is requesting access to Azure resources.
- A role can be assigned to any of these Security Principals

### 2.3 Scope

- Set of resources that the access applies to allowing limiting of actions that can be performed:
- Can be defined on the following Levels
	- Management Group Level
	- Subscription
	- Resource group
	- Individual resource
	
>[!note]
> Permissions in Azure are inherited from top to bottom hence if permissions are given on a higher level then the Security Principal will have access to all the child nodes.

### 2.4 Roles

- Roles in ARM are:
	- Owner - full permissions
	- Contributor - full permissions but does not allow assigning of roles on RBAC
	- Reader - read only permissions
	- Custom - Custom permissions


>[!Tip]
>Azure Resource manager endpoint
>{HTTP method} https://management.azure.com/{version}/{resource}?{query-parameters}


## 3. Office 365 

- Microsoft Enterprise applications i.e Teams, exchange, office
- Cloud based
- Divided into:
	- Admin Portal 
	- User portal
