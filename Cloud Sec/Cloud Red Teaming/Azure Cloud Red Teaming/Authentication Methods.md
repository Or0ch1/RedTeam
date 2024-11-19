- Different ways of authenticating to Azure cloud and the credentials needed.

### Azure Cloud Authentication Credentials

![[credentials.png]]


> [!tip]
> Azure portal URL : **portal.azure.com**
> O365 admin portal: **admin.microsoft.com**
> O365 user portal: **office.com**


- To access Azure cloud via CLI we use :
	- Az
	- Az powershell
	- MgGRAPH powershell

- Credentials used to access can be:
1. Username + password (long term access)

```bash
$ az login
# launches web browser to login

$ Connect-AzAccount
# launches web browser to login

# Microsoft graph
$ Connect-MgGraph -Scopes "Directory.Read.All"

```

2. Service principal(App ID + password or certificate)
``` bash
# get credentials and store in variable and login 
$ $cred =Get-Credential [ Where, Username = Application ID & Password = Client Secret ]

$ Connect-AzAccount -ServicePrincipal -Tenant TentantID -Credential $cred


$ az login --service-principal -u ApplicationID -p Password --tenant TenantID
```

3. Access token(App ID + Access token)
```bash
# generate the access token
$ az account get-access-token --resource=https://management.azure.com

# Login
$ Connect-AzAccount -AccessToken AADAccessToken
```



