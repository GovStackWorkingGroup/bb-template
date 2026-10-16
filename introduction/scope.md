---
title: Scope
---

<!--
How to fill this file: see the Specification Framework, chapter "Introductory Chapters" (chapters/introductory_chapters.md), section "Scope".

The scope turns the overview into the boundary of this document. Write it after overview.md: almost every statement here is derived from one there.

| Overview section                                 | Becomes, in this file                                                    |
|--------------------------------------------------|--------------------------------------------------------------------------|
| System under test                                | Subject and applicability                                                |
| Place in larger systems                          | Relationships                                                            |
| Functionalities                                  | Covered, one entry per functionality, with the same names                |
| Functionalities considered and placed elsewhere  | Not covered, with the owner of each                                      |
| Actors marked Outside                            | Not covered, with the publication in "Specified where" as owner          |
| Interfaces whose contract is defined elsewhere   | Covered: this side of the interface. Not covered: the counterpart        |

When the overview changes, review this file against the table above.

Replace every <placeholder> and delete every comment before publication.
-->

# Scope

## Subject and applicability

This document specifies the <Building Block name> Building Block, a software component that <what it is, from System under test>.

It is applicable to any software solution claiming conformance to `<govstack:spec:bb:identifier>`.

## Relationships

This document extends `<cross-functional requirements identifier>`. A conformant solution meets the requirements of both.

The <Building Block name> Building Block performs the <role> role in `<govstack:ra:identifier>`.

<!-- Repeat the line above for each Domain Reference Architecture named in "Place in larger systems". If none exists, say so. -->

## Covered

<!-- One entry per functionality, with the same name as in overview.md, and the aspect of it this document treats. Add the interfaces whose contract this document defines, if the list does not already make them obvious. -->

- <Functionality name>: <the aspect this document treats>
- <Functionality name>: <the aspect this document treats>

## Not covered

<!--
Every excluded item names its owner. Record five kinds of item:

- Actors outside the boundary: owned by the Domain Reference Architecture, or the counterpart's own specification
- Functionalities placed elsewhere: owned by another Building Block specification, or a gap recorded in a Domain Reference Architecture
- Adjacent Building Blocks: owned by that Building Block's specification
- Layers outside the technical one (policy, legal effect, governance): owned by PAERA, a Guide, or the adopting government
- Government services that use the Building Block: owned by the country's Digital Service System, not a GovStack publication

Include an item only if a competent reader could plausibly have looked for it here. Do not list cross-functional concerns: they are inherited through the extension.
-->

| Excluded | Owned by |
|---|---|
| <Excluded item> | <`govstack:...` \| The adopting government \| ...> |

## Ownership

This specification is owned by the <Working Group name> (`<govstack:team:identifier>`). Change requests go to <where: repository issue tracker, mailing list>.

<!--
Checks before publication (overview.md and scope.md together):

- [ ] The Purpose names at least one capability, and every capability is realised by a functionality
- [ ] Every functionality in the overview has a file in requirements/, with the same name
- [ ] Every actor in the functionality map appears in the actor table, and every arrow crossing the boundary appears in the interface table
- [ ] Every interface is realised by at least one requirement
- [ ] Every actor marked Outside, and every functionality placed elsewhere, appears in "Not covered" with an owner
- [ ] Neither file contains a requirement, a product name or a vendor name
-->
