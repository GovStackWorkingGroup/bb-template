# 9 Workflows

{% hint style="success" %}
A workflow provides a detailed view of how this building block will interact with other building blocks to support common use cases.

This section lists workflows that this building block must support. Other workflows may be implemented in addition to those listed.

The workflows should provide a name and description as well as a sequence diagram that shows the interactions between actors and various building blocks

_Note: Workflows may be categorized into categories where appropriate_
{% endhint %}

_\<Example Workflow>_

### Consenting at initial registration (Pre-registration) using a centralised ID system

The first and somewhat unique use-case is related to the need for consent when the Individual is not yet provisioned in the System processing the data. In such cases, the workflow requires the creation of a valid and trusted Foundational ID to be linked with the Consent Record. Below is shown how a pre-registration use of consent workflow works.

```mermaid
sequenceDiagram

actor Individual
Individual->>+Application: Invoke registration workflow
Application->>+Workflow BB: Trigger registration workflow

note over Workflow BB: Identifies the need for consent

Workflow BB->>+Consent BB: Fetch consent agreement (Registration)
Consent BB-->>-Workflow BB: Returns consent agreement
Workflow BB-->>-Application: Returns consent agreement
Application-->>-Individual: Show consent agreement to fetch data 

note over Individual: The individual agrees<br />to the consent agreement 

Individual->>+Application: Accept consent agreement
Application->>+Foundational ID: Redirect to Foundational ID UI

Foundational ID-->>-Individual: Return Foundational ID authentication UI
Individual->>+Foundational ID: Provide credentials to perform authentication
Foundational ID-->>-Application: Return Foundational ID token (e.g. JWT token) 

note over Application: Foundational ID token recieved<br />is the proof of consent

Application->>+Workflow BB: Fetch data workflow
note right of Workflow BB: Fetch data, <br />For e.g. a population regsitry.

Workflow BB-->>-Application: Confirms the workflow
Application-->>+Workflow BB: Record consent against consent agreement (Foundation ID token, Appl user ID)
Workflow BB-->>+Consent BB: Record consent against the consent agreement
Consent BB-->>-Workflow BB: Return consent ID
Workflow BB-->>-Application: Return consent ID
Application-->>-Individual: Confirm registration

note over Foundational ID: Individual is registered
```
