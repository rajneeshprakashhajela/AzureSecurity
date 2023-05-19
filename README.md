![image](https://github.com/rajneeshprakashhajela/AzureSecurity/assets/43515480/07e491ba-e9bc-444d-ad68-582d6b57a0a8)
![image](https://github.com/rajneeshprakashhajela/AzureSecurity/assets/43515480/6c27a8de-18c6-4d91-8ed6-93631ce5bf2c)
<img width="243" alt="image" src="https://github.com/rajneeshprakashhajela/AzureSecurity/assets/43515480/a58c8e25-3efa-4374-a29b-37ee69ede36d">

![image](https://github.com/rajneeshprakashhajela/AzureSecurity/assets/43515480/c6e0c441-ef58-4d3c-9d48-7151cc0f4e15)


Azure B2B (Azure resouce for support user - As a Guest User) - They are restricted.. (Secure resource)
          Guest User we invite via Email (we fill Guest User Mail id only.. not require other all info)
          
Azure B2C - example Facebook, (Manage identity of User)
Onpremise, Office 365, Hosted in azure app service

![image](https://user-images.githubusercontent.com/43515480/229138369-4afa2f46-f5c1-4c3a-b89c-69152d49d022.png)
![image](https://user-images.githubusercontent.com/43515480/230782928-8ad09d92-31a6-4cfe-923b-d2c3c19f9ffd.png)

![image](https://user-images.githubusercontent.com/43515480/230782916-33850a19-1540-4d98-a49c-4fbd0f179a57.png)
![image](https://user-images.githubusercontent.com/43515480/230782942-6b1e497d-1e1d-4bcf-b5d5-778dd9292123.png)
![image](https://user-images.githubusercontent.com/43515480/230782944-ee81ffa5-e728-49aa-9c93-bf53f38a6e94.png)
![image](https://user-images.githubusercontent.com/43515480/230782949-f35fc3dc-eece-4675-aca2-fa89bea1a6a3.png)
![image](https://user-images.githubusercontent.com/43515480/230782957-2d1227e6-18d1-4756-9223-de0051343caf.png)


![image](https://user-images.githubusercontent.com/43515480/229140703-7e78c287-c13f-4d36-874c-5e099288ba87.png)
![image](https://user-images.githubusercontent.com/43515480/229140997-dba465fb-201d-4c87-b483-8505bd133d25.png)
![image](https://user-images.githubusercontent.com/43515480/229141101-9196f1e3-9380-40e6-b303-a7295c24e61e.png)
![image](https://user-images.githubusercontent.com/43515480/229141161-02094dd2-c77f-4a37-8506-e7827cac435c.png)
![image](https://user-images.githubusercontent.com/43515480/229141749-128a8087-843a-45b9-99e9-b6969d35c0fa.png)
![image](https://user-images.githubusercontent.com/43515480/229142019-0a94ade7-0d67-4619-b622-aaabdc75c25f.png)
![image](https://user-images.githubusercontent.com/43515480/229142198-021eceb9-af09-4613-9305-7fcbb334447a.png)
![image](https://user-images.githubusercontent.com/43515480/229143075-cb939f9a-56c1-43b7-bf4e-74ec8f0f7b4d.png)
![image](https://user-images.githubusercontent.com/43515480/229143152-7ee095c8-e143-4234-b0a3-6b037efd9ad3.png)
===========
<b>Steps for create Group and Bind User in group: </b>

Add New Group --> Group Type(Security, office 365) choose security --> Group Name - (Mention Name) --> Member (Internal or External User)

<b>Application Proxy</b>  -- Azure Ad premium license
Prepare VM TLS 1.2
==============
<b>OnPremise to Azure AD Connect</b>
Steps:
1. Create Azure Active Directory -   Organization name: Hajela, Initial Domain Name: Hajela, Country: India and Global admin User
2. Open Azure portal using created active directory resource.
3. Create Virtual Machine --> (Resource Group - rggroup, Virtual Machine - OnPremiseAD, Image- Windows server 2016 DataCenter) B2(8 GB Memory) , User Name, Password , Inbound Port (HTTP(80), HTTPS(443), SSH(22), RDP(3389)) 

4. Install Active Directory Domain Services on VM <br/>
   Open VM --> Click on Add Roles and Features--> Add Active Directory Domain Service (ADMS) --> .NET Framework --> Install
   Add New User --> User --> New User 
   
5. Download AD Connect on Same VM <br/>
    AD Connect Download--> go to Connect Azure AD-->Use existing AD account (Username ,password) <br/>
    Sync all domain and OUs(organization Unit)
    forest -- hajelaad.net (AzureAD)
    
    
    Useful links to documentation related to AAD
User default permissions

https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/users-default-permissions
The Restrict non-admin users from creating tenants option is shown below
![image](https://user-images.githubusercontent.com/43515480/229164641-3d185c41-520b-4891-be5a-a7078344b18d.png)


Self service password reset

https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-howitworks
![image](https://user-images.githubusercontent.com/43515480/229164752-64b9ce43-faee-4d1b-b4cd-032f578e29d7.png)
![image](https://user-images.githubusercontent.com/43515480/229164828-5f6ee80e-2796-4e06-921f-f8420ae4ea2b.png)

On-premises integration
If you have a hybrid environment, you can configure Azure AD Connect to write password change events back from Azure AD to an on-premises directory.

![image](https://user-images.githubusercontent.com/43515480/229164977-2a98101e-ae25-4702-b493-37fc9fbd1c9a.png)


Cloud based multi-factor authentication

https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-getstarted



Application management in Azure AD

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-application-management
![image](https://user-images.githubusercontent.com/43515480/229165557-f8d32dc0-32e8-4227-8a95-28f118ff09a5.png)

MyApps Portal

https://docs.microsoft.com/en-us/azure/active-directory/user-help/my-apps-portal-end-user-overview

Publishing an on-premise app into AAD using application proxy

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-on-premises-apps

Single sign-on

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-single-sign-on

AD connect

![image](https://user-images.githubusercontent.com/43515480/229165764-f71b7081-c166-4f30-888a-fb7df8255edb.png)
![image](https://user-images.githubusercontent.com/43515480/229165835-eb6f2d4a-a698-4f77-ba55-90b91376180b.png)

Single forest, single Azure AD tenant
![image](https://user-images.githubusercontent.com/43515480/229165918-04bb66a8-8587-4ef3-809e-bbbfb0282f3d.png)

Single forest, multiple sync servers to one Azure AD tenant
![image](https://user-images.githubusercontent.com/43515480/229166055-be86af73-27a5-48eb-a5fc-bd988e007bf6.png)
Multiple forests, single Azure AD tenant
![image](https://user-images.githubusercontent.com/43515480/229166125-8be17400-4d2e-4d5a-bad0-e539b8edeb5b.png)


Multiple forests, multiple sync servers to one Azure AD tenant
![image](https://user-images.githubusercontent.com/43515480/229166203-8a7e7499-611b-402e-be93-2f393ca98627.png)


https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect

https://docs.microsoft.com/en-us/azure/active-directory/hybrid/plan-connect-topologies




<H>Location Based Condition Access Policy </H>
Steps:
go to Azure portal --> Azure Active Directory --> Conditional Access -->Policies <br/>
Named Location -->(IP range Or country) --> IP Range - .........204/32  <br/>
Click on MFA --> and mention IP address <br/>
<br/>
Assignment -->  <br/>
1. User & group Selected <br/>
2. which app for condition access policy  <br/>
3. Cloud app selected - Microsoft planner <br/>
4. Condition
            
<b>Role Base access control </b> <br/>
 1. Security Principle (Represent User, Group, Service Principle or managed identity(Auto manage by azure AD) <br/>
 2. Role Definition (Collection of permission)<br/>
 3. Scope (Inside Role, If you want to define limit the actions allowed by defining a scope<br/> 


Multiple Way
1. User --> Directory Role --> Limited Administrator (Admin, Developer, billing Admin)
2. Resource Group--> Access control(IAM)(Owner, contributer, Reader)
3. Subscription level --> Aztraining-->Access control(IAM)(Owner, contributer, Reader) --> Add Role Assignment--> (Add User)
  
  
  <h1>For Custom Role  </h1><br/>
  1. Open PowerShell and mention Azure User and password<br/>
  2. Example - We don't want to delete storage account<br/>
  3. Get AzRoleDefinition Name "StorageAccountContributer" (New Custom Role) <br/>
  4. Get AzRoleDefinition Name "StorageAccountContributer" | Convert to JSON | out-file "c:\user\customStorage.JSON"<br/>
  5. Open JSON File "Action" and "NotAction" mention <br/>
  6. "NOTAction":[ "Microsoft.Storage/StorageAccounts/Delete"]<br/>
  7. Get-AzSubscription<br/>
  8. New-AzRoleSubcription InputFile "c:\user\customStorage.JSON"<br/>
  9. for checking custom Role --> Go to IAM --> Go to Roles Tab--> (you will find defined custom role)<br/>
  10. Assign Role to User (not delete any resource)<br/>
  11. Add --> Add Role Assignment--> Role Name , User name  (save)<br/>
  12. check in Role Assignment <br/>
  
 
     
   
  <h1>Group creation and Role Assignment  </h1><br/>
  Security Group (Dynamic Group), Role Definition (Built in Role), Scope (Storage Account)
  Group --> Member (all Users) , Owner (Admin) - we can add using add Owner
  Group Membership 
  Application 
  Licenses - Group level 
  Azure Resources
  Audit logs
  
  <h1>Dynamic Group creation and Role Assignment  </h1><br/>
  Group --> Create Group --> StorageAdmin
  Go to created Group (StorageAdmin) --> check membership processing status (Update completed)
  Go to Storage account--> Access Control (IAM) --> Add Role Assignment --> Role (contributer)  and select group (StorageAdmin) we created --> (save)
  
  Now mentioned User can use their credential and can see storageaccount and other group and role related info
   
  
   <h1>Azure AD App Registration </h1><br/>
  
  
<img width="727" alt="image" src="https://user-images.githubusercontent.com/43515480/230776880-ff8eff4c-23a1-43a0-9634-0a41e8d30763.png">

<img width="728" alt="image" src="https://user-images.githubusercontent.com/43515480/230776941-4f726ef4-416d-476e-bf5a-e70f59165e76.png">
