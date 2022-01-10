# Overview
This guide highlights the various options provided in the reference UI implementation of the registration client.

## Know your machine TPM keys
A Trusted Platform Module (TPM) is a specialized chip on a local machines that stores RSA encryption keys specific to the host system for hardware authentication.The pair is maintained inside the chip and cannot be accessed by software. By leveraging this security feature every individual machine would be uniquely registered and identified by the MOSIP server component with it's TPM public key.

To extract the TPM public key, use the ![TPM key extractor utility](https://github.com/mosip/mosip-infra/blob/develop/deployment/sandbox-v2/utils/tpm/key_extractor/README.md).

## Pre-requisites to onboard machine, operator
The Admin needs to:
1. Create and activate the registration client machine using Admin portal.
2. Create a user/operator account in Keycloak
3. Assign the operator a role of either the Supervisor or Officer using the Admin portal.
4. Finally, perform the User Zone mapping and User Center mapping in the Admin portal.
 
 ## Registration client setup
To setup the registration client:

**System prerequisites**
* CPU - Dual Core Processor - 2GHZ  
* RAM - 16 GB  
* Local Storage Disk Space - 500 GB 
* USB 2.0 ports or equivalent hub.  
* Physical machine with TPM 2.0 facility.   
* Windows OS [10 v] 

![Setting up the registration client](https://github.com/mosip/registration-client/blob/develop/README.md)

### Launching the registration client
the operator needs to click on run.bat to launch the client.
Client always launches with the pre-loader screen which displays the information about the network status,  build status verification, online status, etc.

<< screenshot of pre-loader  only>>

1. First time launch
- After the pre-loader, the login screen is displayed.
- Any valid operator credentials can be provided to authenticate and start the initial sync.
- On successful intial sync, the operator will be prompted to **restart** the application.
- After the first launch, the operator can notice .mosipkeys and db folder created under the registration client setup folder.

Note: Deletion of the .mopsipkeys or the db folder makes the application get into an invalid state and hence will fail to launch. To be able to launch the client again, the operator should make sure that both the folders are removed. 
<< restart image>><< setup folder structure>>
![](_images/reg-client-pre-loader-success.png)

2. On the next launch after the initial sync,
  - The registration client login page provides the operator an option to select the language for viewing the registration client UI.
  - After successful login, the operator either lands into the operator onboard page or the home page.
    For more details on operator onboarding, refer to ![Operator onboarding guide](operator-onboarding.md).
    For more details on Home page, refer to <>

### Modes of operation
      
* **Offline**- Operator can use the reg client in offline mode to only do the registrations and EOD process. During offline, operator authentication will be based on locally saved password hash. An operator can work in offline mode only if they have logged into to the reg client being online atleast once.
* **Online**- Machine must be online for the registration client first launch. For any server-client sync or vice-versa, the reg client must be online. In the online mode, the client reaches out to the server for passowd authentication.
       
**Note**: On successful onboard of the operator, biometric templates of the operator are stored locally.
       Biometric authentication does not reach out to the server everytime instead it is validated based on the locally stored templates on the reg client machine. 
