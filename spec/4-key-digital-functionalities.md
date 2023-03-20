# 4 Key Digital Functionalities

{% hint style="success" %}
The Key Digital Functionalities describe the core (required) functions that this building block must be able to perform. These functionalities should be described as business processes as opposed to technical specifications or API definitions.&#x20;

This section should contain 2 sections. The first provides an overview of functionality that should be provided by the Building Block. The second outlines the design of the building block and any components that make up the Building Block

Note, this section may be extended after the key functionalities have been listed to include any assumptions or context that is needed.&#x20;
{% endhint %}

_\<Example Key Digital Functionalities (based on ID Building Block)>_

## 4.1 Overview of ID Building Block Functionality

The ID Building Block provides secure foundational identification services for a system.&#x20;

* The ID Building Block provides foundational identity services. Authentication is not provided by this Building Block
* Foundational IDs come with no specified purpose or attached entitlement but functionalities simply let an entity prove who it is
* Captures only limited information about users, such as name, date of birth, address and gender
* For a given set of credentials, fetches a corresponding ID if it exists in the registry
* Uses different biometric methods to identify and authenticate users through means other than user photographs (eg fingerprints, iris scans, facial recognition) to ensure there are no duplicates or fakes, creating a highly trustworthy database
* Used to enable services such as opening bank accounts, buying SIM cards, receiving entitlements from the government, signing forms electronically, investing in mutual funds and getting credit
* Incorporates privacy into its design when the purpose of the authentication is not revealed if a service provider sends an authentication request.

## 4.2 Design and Components of ID Building Block

The diagram below shows the high-level view of the Identity and Verification Building Block.

![Identity and Verification Building Block offers 5 different external APIs:](broken-reference)

**Abstract**

Identity and Verification Building Block offers a set of external services to the other Building Blocks:

* **Federation services** are there to federate and harmonize multiple identities, which is creating a link between various digital identities that an individual may have.
* **Enrollment Services** allow to on-board of new identities for individuals, which means collecting their personal identity data, evidence of them, and biometrics.
* **ID/Credential Management Services** permit to issue and manage the life cycle of Identity credentials, those services will allow to issue identity documents, to manage their renewal, or declare them as stolen.
* **Identity Verification Services** allow a service provider to verify an identity or some of its attributes, for example checking a person's declared identity or verifying its age.
* **Notification services** will allow a third party to subscribe to events occurring on identity and to receive notifications, useful to inform external functional Building Block when a person was born or has passed off so that the external system can take required actions.
