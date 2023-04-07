# 4 Key Digital Functionalities

{% hint style="success" %}
The Key Digital Functionalities describe the core (required) functions that this building block must be able to perform. These functionalities should be described as business processes as opposed to technical specifications or API definitions.&#x20;

This section should contain 2 parts. The first provides an overview of functionality (Key Digital Functions or KDFs) that should be provided by the Building Block. These KDFs should be organized by area of functionality and should be numbered so that they can be referenced in other sections.

The second outlines the any components that make up the Building Block. Many Building Blocks are made up of multiple components. These can be described (and diagrams provided where appropriate) in this section.

Note, any assumptions or context that are needed for this Building Block should be provided in Section 2 (Description).&#x20;
{% endhint %}

_\<Example Key Digital Functionalities (based on Consent Building Block)>_

## 4.1 Consent Building Block Functionality

These functionalities are derived from the [consent agreement lifecycle](broken-reference) and categorised according to the [Actors](broken-reference) described above. While the consenting workflows (as described above) are implicitly considered the centerpiece of the Consent Building Block, it is important to realise that the integrity of consent management can only be achieved if robust configuration before and auditing after the Consent Agreement signing and Consent Record verification activities are in place. Hence, the functionalities are described following the logical sequence of the consent agreement lifecycle and they are all equally important components of the Consent Building Block.

### 4.1.1 Administrative Functions

It is foreseen that one organisation involved in the data processing transaction takes responsibility for the configuration of the Data Policy and respective Consent Agreements(s), and so the organisation’s Administrator maintains the required configurations.

* An Organisation Administrator can Create, Update, Read, or Delete a Consent Agreement based on the Data Policy requirements.
* The Consent Building Block must provide Notifications for Data Providing and Data Consuming Systems, as well as Individuals upon changes to Agreement or Policy configuration.

### 4.1.2 User Functions

An individual user must be able to interact with the Consent Building Block to provide or withdraw consent.

* An Individual can view a Consent Agreement and the conditions for personal data processing (with adequate clarity for informed understanding). This includes obtaining copies of the consent agreement.
* An individual can sign a Consent Agreement during a data sharing workflow. Note that this can also happen offline without data sharing in place.
* An individual and update or withdraw consent from a Consent Agreement
* The Consent Building Block must provide notifications for these user interactions

## 4.2 Design and Components of ID Building Block

The Identity and Verification Building Block consists of a set of Services or Components which are used to provide necessary functionality to other Building Blocks

* **Federation services** are there to federate and harmonize multiple identities, which is creating a link between various digital identities that an individual may have.
* **Enrollment Services** allow to on-board of new identities for individuals, which means collecting their personal identity data, evidence of them, and biometrics.
* **ID/Credential Management Services** permit to issue and manage the life cycle of Identity credentials, those services will allow to issue identity documents, to manage their renewal, or declare them as stolen.
* **Identity Verification Services** allow a service provider to verify an identity or some of its attributes, for example checking a person's declared identity or verifying its age.
* **Notification services** will allow a third party to subscribe to events occurring on identity and to receive notifications, useful to inform external functional Building Block when a person was born or has passed off so that the external system can take required actions.
