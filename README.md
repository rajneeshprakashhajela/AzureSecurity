Azure B2B (Azure resouce for support user - As a Guest User) - They are restricted.. (Secure resource)
          Guest User we invite via Email (we fill Guest User Mail id only.. not require other all info)
          
Azure B2C - example Facebook, (Manage identity of User)
Onpremise, Office 365, Hosted in azure app service

![image](https://user-images.githubusercontent.com/43515480/229138369-4afa2f46-f5c1-4c3a-b89c-69152d49d022.png)
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

Self service password reset

https://docs.microsoft.com/en-us/azure/active-directory/authentication/concept-sspr-howitworks

Cloud based multi-factor authentication

https://docs.microsoft.com/en-us/azure/active-directory/authentication/howto-mfa-getstarted

Application management in Azure AD

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-application-management

MyApps Portal

https://docs.microsoft.com/en-us/azure/active-directory/user-help/my-apps-portal-end-user-overview

Publishing an on-premise app into AAD using application proxy

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/application-proxy-configure-single-sign-on-on-premises-apps

Single sign-on

https://docs.microsoft.com/en-us/azure/active-directory/manage-apps/what-is-single-sign-on

AD connect

https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-azure-ad-connect

https://docs.microsoft.com/en-us/azure/active-directory/hybrid/plan-connect-topologies
    
     
   
