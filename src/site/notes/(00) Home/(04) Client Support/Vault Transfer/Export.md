---
{"dg-publish":true,"permalink":"/00-home/04-client-support/vault-transfer/export/","title":"Vault Export"}
---


> [!DonorPerfect Clients: All vault export requests for DP clients should be directed to the client’s ==Account Manager==. The AM will use the opportunity to see if we can retain the client. If not, they will review the **$625 export fee that is charged in addition to the SafeSave/NMI transfer fee** listed in the sections below and create a Salesforce Opportunity for the export. The AM should also make the client aware that there will be a fee charged by SafeSave, but SafeSave can review the details of that fee as it can vary depending on the number of records being transferred.] 


> [!Non-DonorPerfect Clients: If a vault export is requested by a non-DonorPerfect client, the request should be emailed to [support@safesavepayments.com](mailto:support@safesavepayments.com "mailto:support@safesavepayments.com") with the subject “Vault Export - [Org Name]”]


## US Clients

### Vault Transfer Fee:

|   |   |
|---|---|
|**Record Count**|**Price**|
|1-1000|$500|
|>1000|$0.50 per record|

While it is technically possible, we no longer do partial transfers as standard; we send all vault contents to the new processor. If the client wanted to remove records prior to the transfer, they could. However, since there is a $0.30 vault fee, doing so will not affect the cost of the transfer if the record count. In fact, it will increase the overall cost.

We changed this policy in order to reduce the risk of vault records being missed from the transfer. We can make exceptions in certain circumstances (e.g the client has a very large number of records or expired cards). In this case, we would export the vault info from the gateway, ask the client to edit it to contain only the records they would like included in the transfer, and send it back to us. This should not be standard practice, however.

## Reviewing Transfer Details with the Client:

When a merchant wants to transfer vaulted card information to another processor:

- Create a case in Salesforce, if one does not already exist
    
    - Subject = “Vault Export - [Client Org Name]
        
- Fill out any relevant data that you already have about the transfer on the Data Export Request form. This should at minimum be the number of vault records the client currently has, and the calculated transfer fee. ( Form is in the attachments of this confluence page)
    
- Send the following email to the client, making sure to add the number of stored cards and transfer fee. Be sure to alter this email if some of the of the requested information was already provided by the client.
    

> Hi ,
> 
> I've been informed that you are interested in transferring the payment data stored within your SafeSave Vault to a different processor. There are a couple items that I need to address to help you with that.
> 
> - We would need to know which processor/gateway you're transferring the cards to
>     
> - A copy of that processor/gateway's most recent Attestation of Compliance (AoC)
>     
> - That processor/gateway's public PGP key which we can use to encrypt the data with
>     
> - An email address or SFTP credentials to where the data can be sent/dropped off
>     
> - I have attached our PGP key [here](https://secure.nmi.com/merchants/Import-PGP.asc "https://secure.nmi.com/merchants/Import-PGP.asc"). Your new processor can use this to encrypt SFTP credentials, if needed
>     
> - Also our AoC can be found here, if your new processor requires it: [Security & Compliance](https://www.nmi.com/solutions/security/ "https://www.nmi.com/solutions/security/")
>     
> - SafeSave does not alter or audit the contents of your vaulted data; all payment methods stored in the vault at the time of the transfer will be sent to your new processor.
>     
> - You currently have ____ cards stored. The transfer fee will be ____. The transfer fee would be billed via automatic ACH, like your SafeSafe gateway billing is.
>     
> - Please fill out and sign the attached card data export request form. The completed form can sent back in this email chain. 
>     
> - If you would like to copy a representative with your new gateway/processor onto this email chain, we can work with them directly to facilitate the transfer.
>     
> 
> If you have any follow up questions for me, please let me know.
> 
> Regards,  

- Once the client and/or other processor has provided the email or SFTP information and confirmed the the transfer fee, the NMI transfer request form can be filled out.
    

## Requesting NMI to Start the Transfer:

- NMI’s transfer form can be found here: [![](https://supportforms.nmi.com/favicon.ico)NMI Data Transfer Request Form](https://supportforms.nmi.com/223106026095043)
    

|   |   |   |   |   |   |
|---|---|---|---|---|---|
|**Affiliate Name**|**Affiliate Username**|**Affiliate ID**|**Authorizer Name**|**Authorizer Email**|**Contact email**|
|SafeSave (Partner)||4843|#Your Name#|#Your Email#|Support@SafeSavePayments.com|
|DonorPerfect [Payfac]|DPEasyRate|5235|||[Support@SafeSavePayments.com](mailto:Support@SafeSavePayments.com "mailto:Support@SafeSavePayments.com")|
|DonorPerfect [Legacy]|dpo111|946|||[Support@SafeSavePayments.com](mailto:Support@SafeSavePayments.com "mailto:Support@SafeSavePayments.com")|
|DonorPerfect [Canada]|accounting|1708|||[Support@SafeSavePayments.com](mailto:Support@SafeSavePayments.com "mailto:Support@SafeSavePayments.com")|
|Court Reserve|CourtReserve|10895|||[Support@SafeSavePayments.com](mailto:Support@SafeSavePayments.com "mailto:Support@SafeSavePayments.com")|
|Watertight|KDSMOSES|3691|||[Support@SafeSavePayments.com](mailto:Support@SafeSavePayments.com "mailto:Support@SafeSavePayments.com")|
|JR - Fees to SW|JRBilltous|3112||||
|SafeSave Payments  <br>[JR Legacy]|safesave|1565||||
|Jackrabbit|JackrabbitPayFac|5431||||

- Enter Merchant (gateway) Name and Gateway ID
    
- **“**What data will be exported?” = All Customer Vault Records
    
- Enter Receiving Entity Information
    
    - Receiving entity name = Name of the new processor
        
    - AoC: You should have a copy provided from your original email to the client/processor. Any new AoC’s should be added to the attachments of this page
        
    - Receiving Entity's Public PGP Key (URL) = webpage where the new merchant’s PGP key can be found.
        
    - Receiving Entity's Public PGP Key (File): A .txt file of the PGP key block
        

Any new AoC’s, PGP URLs, and PGP Key Files should be added to the Processor Transfer Info Confluence page in their respective section.

For the PGP Key file, you will need to copy the code block into a text editor such as notepad and save it as a .txt file to attach it to the form. Example (truncated) block below:

-----BEGIN PGP PUBLIC KEY BLOCK-----

mQINBF0dLOEBEADMhdKpL6HmgV3rGuW/Qj9by6I/bdCOX9HrGf6MNXr00rtOKSQ5  
KpM6pacMxXeaUKXgKGiU6gFWq3r6NXLRcKCmTGlnyuS2gI1Pv6R3uo+tjzeuRhiR  
dKFiGDZOcreZ7b2x6q4DmpAIdf4mnVwHvLT2IeZBIDb/VlZnyIBBtUiTohmL6rVp  
waAsjutd9tmnAQg/Mu/Y4C2QArr2Bqy9XlD1osyqBBOaWLKM/opoh4gpxSH90f5C  
ymAZykMMk8EnPQ6F8lro6BFkOSw1wu47fBijf7pq1a15JyoA66UkPmCXiuV0XrJc  
k6stzjh1zPBrhdtcQ6TaDsyxoPCzLJ4I38SSGtXdJ+jfn8WTt1Qbl4JSI1UfrbSL  
nnoaAnKjy4H5q3MI7o3b87IKYe4zzFn0vPU4xOaT7AJNPu0x/BBk0bGFGw37i8+5  
6FXmb+wWloT1aCA5GzpvmYGrQNK2aI2vCTlOg0IJJJzLCXpar4RzB5mSFoxaRlC/  
VW5o2TndrWmQKW0yiAlTefh1Kk88h8E0bCVcklaTTaXkNk5OJJiVvf2XjbIPcKoq  
mQ7N0ExfEiDQhgmABbG3KmWjHjvciaMsxVKYE1nBOhyPXaT3BRuKbOcyhWX8SF07  
B31Awq/WKhMH/S6LZOqg9ui7UyohS1XkLiFhlPOStkK4Hn77guVidsTARQARAQAB  
tDdTdHJpcGUgSW1wb3J0IEtleSAoUENJKSA8c3VwcG9ydC1taWdyYXRpb25zQHN0  
cmlwZS5jb20+iQJUBBMBCAA+AhsDBQsJCAcCBhUKCQgLAgQWAgMBAh4BAheAFiEE  
rr98SDjETS/cmaP5nHi3Ygwema0FAmQ194sFCQlqDaoACgkQnHi3Ygwema1+4Q//  
Sq+8tlV6SkcCmYlO2j3/2bp8PGcQUizEqxb1R6BNfT8astbAxUw47AYtb2TG7+W [….]  
-----END PGP PUBLIC KEY BLOCK-----

- Select correct send method
    

Most often this will be “Upload to Their SFTP”

- Receiving Entity's SFTP Credentials: This will be username/password info (in the form of a code block, like above) that has been encrypted with NMI’s PGP key. You will again need to use an editor to save the block as a .txt file.
    
- Enter the total number of vault records in the gateway
    
- “Who will we bill for this Data Export?” = The Merchant
    
- Enter in any special instructions/notes, click the checkbox “I confirm I have filled in this form as accurately as possible.”, and Submit
    

Once you receive confirmation from NMI that the transfer is complete, email the client/new processor with confirmation of the number of records included in the transfer and the name of the file that was dropped off (NMI will provide these in their confirmation email)