---
title: Scope
---

<!--
How to fill this file: see the Specification Framework, chapter "Introductory Chapters" (chapters/introductory_chapters.md), section "Scope". A complete worked example is in resources/examples/wallet/introduction/scope.md of the same repository.

The scope is read after purpose.md and before technical_overview.md, but written last: almost every statement here is derived from one of the other two. The Specification Framework's preparatory work guide (resources/preparatory_work.md, "Reading order and writing order") shows which section becomes which part of this file. When purpose.md or technical_overview.md changes, review this file against it.

Replace every <placeholder> and delete every comment before publication.
-->

# Scope

## Subject and applicability

<!-- Say what the Building Block is, where its boundary sits and how it is assessed. The subject is a software component, never a government service, a person or an organisation. The rest of the specification calls the software inside this boundary the Building Block software. Do not describe the internal architecture of a solution. -->

This document specifies the <Building Block name> Building Block, a software component that <what it is and does>.

Its boundary includes <what is inside>. It excludes <closely related things that are outside>.

The <Building Block name> is assessed as a black box, through its interfaces. <What cannot be observed from outside, and is therefore verified by audit.>

It is applicable to any software solution claiming conformance to `<govstack:spec:bb:identifier>`.

<!-- If the specification has no extensions, delete the paragraph and list below. Otherwise list each extension declared in metadata.yml, with what it adds and the extensions it requires. -->

A conformant solution meets the core of this document. It may also claim one or more of these extensions, and meets every requirement of each extension it claims:

- <Extension>: <what it adds>. <Requires <Extension>, if any.>

## Relationships

This document extends `<cross-functional requirements identifier>`. A conformant solution meets the requirements of both.

The <Building Block name> Building Block performs the <role> role in `<govstack:ra:identifier>`.

<!-- Repeat the line above for each Domain Reference Architecture named in "Place in larger systems". If none exists, say so. If the role is performed in full only by solutions that claim an extension, add ", when it claims the <Extension> extension". -->

## Covered

<!-- One entry per functionality, with the same name as in technical_overview.md, and the aspect of it this document treats. Add the interfaces whose contract this document defines, if the list does not already make them obvious. Group the entries under the core and each extension; without extensions, drop the headings. An obligation towards a role that sits in an extension is covered, under that extension; only the counterpart's behaviour is not covered. -->

**Core**

- <Functionality name>: <the aspect this document treats>

**<Extension> extension**

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
Checks before publication (purpose.md, scope.md and technical_overview.md together):

- [ ] The Purpose names at least one capability, and the capabilities it names are those declared in metadata.yml, with the same titles
- [ ] Every capability is realised by at least one functionality, and every functionality realises at least one capability. The Realises column matches the realises field of each file
- [ ] A capability realised only by extension functionalities is said to be so in the Purpose
- [ ] The scope states what the Building Block is and where its boundary sits
- [ ] The Market assessment says what was surveyed and why it led to the functionalities listed
- [ ] Every functionality in the Technical Overview has a file in requirements/, with the same name
- [ ] The Conformance column of every functionality matches the conformance and extension fields of its file, and the extensions listed match those declared in metadata.yml
- [ ] A solution that meets only the core is a useful instance of the Building Block, and the Technical Overview says why
- [ ] Every extension has at least one REQUIRED requirement, and appears in the conformance statement and in "Covered"
- [ ] When the actor and interface tables are present, every actor in the functionality map appears in the actor table, and every arrow crossing the boundary appears in the interface table
- [ ] When the interface table is present, every interface is realised by at least one requirement whose interaction field matches the interface type, and every requirement that is not INTERNAL realises a listed interface
- [ ] Every actor outside the boundary, and every functionality placed elsewhere, appears in "Not covered" with an owner
- [ ] None of the three files contains a requirement, a product name or a vendor name
-->
