# Overview

The Registration client is a thick Java-based client where the resident's demographic and biometric details are captured along with the supporting documents in online or offline mode. Data is captured in the form of registration packets and is cryptographically secured to ensure that there is no tampering. The captured information is packaged and sent to the server for further processing.

## Who operates the Registration client?

The Registration client can be operated by an operator who can be either a Supervisor or an Officer. They can login to the application and perform various activities.

**Features accessible to Registration Officer and Supervisor**- Login/Logout, Onboarding, Synchronize Data, Upgrade software, Export packet, Upload packet, View Re-registration packets, Correction process, Exception authentication

**Feature exclusive to Registration Supervisor**– Approve/reject registrations (end-of-day approvals)

To know more about the roles and the onboarding process of an operator, refer to [Operator onboarding](operator-onboarding.md).

## Features
Registration Client collects the demographic and biometric details of a resident at the registration centers and sends the data to the Registration Processor for generating the UIN. Below are some of the features associated with the Registration client:

### Functional features
*	Registering an individual for ID issuance
*	Updating a registered individual’s details
*	Finding an individual’s ID
*	Creating a correction packet
*	Can serve individuals with Pre-registration ID or walk-ins
*	Option to collect demographic, documents and biometric data
*	Support for biometric exception scenario
*	Support for a guardian for registering minors
*	Support for an introducer for individuals without any mandatory documents
*	Support for integration with devices such as a printer, scanner or GPS
*	Issuance of application ID with QR code
*	Officer and supervisor model
*	Option to modify various settings
*	Works in offline and online modes
*	Has the capability to remotely update the software

### Technical features
*	UI and layout can load dynamically based on a configurable UI specifications
*	Data can be captured in multiple languages based on configuration
*	Virtual keyboards can be added to capture data
*	Transliteration engines can be integrated
*	TPM (Trusted Platform Module) is necessary and is used to make sure it is secure and trusted
*	Can collect data in offline mode
*	Can sync the latest master data, configurations, UI-specs, encryption keys and pre-registrations from the server
*	Operators (Officer or Supervisors) can log in using a password, OTP or biometrics
*	Use of SBI (Secure Biometric Interface) for biometric device interfacing
*	Tested on Windows with Oracle JDK 11
*	Registration client UI is a reference implementation and can be changed

## Registration client entity diagram


## Biometrics SDK Implementation
  
  SDK integration guide
  

## Packets


## Registration client UI reference implementation
MOSIP provides a Windows-based reference implementation of the registration client that has a UI and the business logic to perform the above process flows. The code, design, App setup, build documentation is available in **registration client repo**. The App may be modified according to a country's need.
  
To know more about setting up the registration client sample UI implementation, refer to [Registration client user guide](registration-client-user-manual.md).

To know more about the functions present in the Home page of the registration client, refer to [Registration client home page](registration-client-home-page.md).
  
## Configurations
For details related to Registration Client configurations, refer to registration-Client configuration.

## UI Specifications
What is UI Spec, where is the sample available .. 
Default UI Specifications loaded with Sandbox installation is available [here](https://github.com/mosip/mosip-infra/blob/1.2.0-rc2/deployment/v3/mosip/kernel/masterdata/xlsx/ui_spec.xlsx)

