# cloudformation-crossaccount
CF template to create Cross account role in Security Account and Client account. 

***Usage***

---
Login to AWS console of client who wish to give access to Security Account. 

Create Cloudformation stack by running cross-account-client.yaml
This template basically asks for 4 parameters. Other than SecurityAccount Number [ AWS account number curresponds to Security account ], everything is boolean. 

* SecurityAccountNumber
* CreateAdminAccess
* CreatePowerAccess
* CreateReadOnlyAccess

---
 
Login to AWS console of Security Account  

Create Cloudformation stack by running cross-account-security-account.yaml
This template basically asks for few parameters. This creates swtich roles Policy in Security account. 

* ClientAccountNumber
* ClientName
* ProjectName
* Environment
* GrantedAdminAccess
* GrantedPowerAccess
* GrantedReadAccess
