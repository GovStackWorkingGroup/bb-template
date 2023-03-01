# 6 Functional Requirements

{% hint style="success" %}
The functional requirements section lists the technical capabilities that this building block should have. These requirements should be sufficient to deliver all functionality that is listed in the Key Digital Functionalities section.

These functional requirements do not define specific APIs - they provide a list of information about functionality that must be implemented within the building block.

These requirements should be defined by subject-matter experts and don’t have to be highly technical in this section.

The requirements can be shown in table format. Multiple tables can be used to show different functional areas for the Building Block
{% endhint %}

_\<Example Functional Requirements>_

| **Name**                         | **Description**                                                                                                                                                     | **Optionality (REQUIRED, RECOMMENDED, OPTIONAL)** |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| Create Consent Agreement         | It shall be possible to create a consent agreement, either based on an existing or new data policy template. Each consent agreement shall be under version control. | REQUIRED                                          |
| View Consent Agreement           | It shall be possible to view an existing consent agreement                                                                                                          | REQUIRED                                          |
| Update Consent Agreement         | It shall be possible to update an existing consent agreement.                                                                                                       | REQUIRED                                          |
| Terminate Consent Agreement      | It shall be possible to terminate an existing consent agreement                                                                                                     | REQUIRED                                          |
| Revision history                 | It shall be possible to capture and sign all changes to Consent Agreements, Consent Policies and Consent Records in tamper-proof Revisions                          | RECOMMENDED                                       |
| Change notification subscription | It shall be possible to subscribe to enable or disable a change notification towards users                                                                          | RECOMMENDED                                       |
| Change notification              | It shall be possible to trigger a change notification when there are changes done to an existing consent agreement                                                  | OPTIONAL                                          |
| Logging                          | The BB shall log all administrative functions                                                                                                                       | REQUIRED                                          |
