---
title: Overview
---

<!--
How to fill this file: see the Specification Framework, chapter "Introductory Chapters" (chapters/introductory_chapters.md). A complete worked example is in resources/examples/wallet/introduction/overview.md of the same repository.

The overview describes the Building Block. Its content comes from the Working Group's preparatory work: it publishes the result of that work, it does not derive it. If a section cannot be filled, the preparatory work is probably incomplete.

Replace every <placeholder> and delete every comment before publication. Do not write requirements, product names or vendor names in this file.
-->

# Overview

## Purpose

### Value

<!--
Answer four questions in one to three paragraphs:
1. What problem does this Building Block solve, and for whom?
2. What can a government do with it that it could not do before?
3. Which capabilities does it provide? Name each as a noun phrase ("Credential Storage", not "Stores credentials"), stating what, never how.
4. What would go wrong if every government and vendor built this component to their own design? Use one or more of: interoperability, replaceability, choice, assurance.

Declare every capability named here in metadata.yml, under capabilities, with the same title. Every capability must be realised by at least one functionality in the Description, through the realises field of the functionality's file. When a capability is realised only by an extension, say so: a reader must not assume every conformant solution provides it. If none of the four arguments in question 4 applies, the component may not need a GovStack specification.
-->

The <Building Block name> Building Block exists so that <beneficiary> can <outcome>.

Today <the problem, stated plainly>. The <Building Block name> provides **<Capability>**, **<Capability>** and **<Capability>**, so that <the changed state>.

A common specification matters here because <the interoperability, replaceability, choice or assurance argument, specific to this Building Block>.

### Place in larger systems

<!--
Place the Building Block in the systems it operates in. Name roles, not products. Place the reference architecture for the reader; do not import its content.

- The GovStack Architecture, and the cross-functional requirements the Building Block inherits
- Each Domain Reference Architecture in which it performs a role, and the role. If none exists for the domain, say so and describe the domain context in the Building Block's own terms
- Which part of this specification performs each role. The obligations towards a role are in this specification, never in the reference architecture. When they are in an extension, say that only a solution claiming the extension performs the role in full
- The other roles in those systems, and which of them it exchanges information with
- The Building Blocks it commonly works with, and for what
- Whether it is a foundational or a feature Building Block, when that helps the reader
-->

The <Building Block name> operates within the GovStack Architecture, and every conformant solution meets the GovStack cross-functional requirements.

In the <Domain Reference Architecture name> (`<govstack:ra:identifier>`) the <Building Block name> performs the **<role>** role. <The other roles in that system, what each does, and which of them exchange information with this Building Block.>

The <Building Block name> is a <foundational | feature> Building Block. It commonly works with:

- the **<Building Block>** Building Block, <for what>;
- the **<Building Block>** Building Block, <for what>.

<!-- Context diagram: the Building Block as one role among the others, with the main exchanges. Draw roles, not deployments, and keep the Building Block's internals out. Draw one diagram per Domain Reference Architecture. -->

```mermaid
flowchart LR
  subgraph RA["<Domain Reference Architecture> (<govstack:ra:identifier>)"]
    direction LR
    RoleA["<Role>"]
    BB["<Role><br/><b><Building Block name> Building Block</b>"]
    RoleB["<Role>"]
    RoleA -- "<exchange>" --> BB
    BB -- "<exchange>" --> RoleB
  end
```

*Figure 1: the <Building Block name> in the <role> role.*

## Description

<!-- The diagrams and tables below must agree: every actor in the functionality map appears in the actor table, and every arrow crossing the boundary appears in the interface table. -->

### System under test

<!--
State what is assessed when a solution claims conformance. The subject is a software component, never a government service, a person or an organisation.

- What it is, in one or two sentences
- Where its boundary sits: what is inside, and which closely related things are outside
- How it is observed: as a black box, through its interfaces. Note anything that can only be verified by audit

Do not describe the internal architecture of a solution.
-->

The system under test is a software component that <what it is and does>.

Its boundary includes <what is inside>. It excludes <closely related things that are outside>.

The <Building Block name> is assessed as a black box, through its interfaces. <What cannot be observed from outside, and is therefore verified by audit.>

### Functionalities

<!-- One row per functionality. Each has its own file in requirements/, and the name here matches that file's title exactly. Realises names the capabilities from Value the functionality realises, by title, and matches the realises field of the file. Description repeats the description field of the file. Conformance is "Core", or "<Extension> extension", and matches the conformance and extension fields of the file. See the Specification Framework, chapter "Functionalities and Extensions". -->

| Functionality | Realises | Conformance | Description | Requirements |
|---|---|---|---|---|
| <Functionality name> | <Capability> | Core | <One sentence> | `requirements/<functionality-name>.md` |
| <Functionality name> | <Capability>, <Capability> | <Extension> extension | <One sentence> | `requirements/<functionality-name>.md` |

<!-- Explain why these functionalities were chosen. Where several functionalities realise one capability, say how they divide it, and when some of them are in an extension, what a solution claiming it provides beyond the core. Then name the functionalities a reader might expect but that were placed elsewhere: that part becomes the "Not covered" list in scope.md. -->

<Capability> is realised by <Functionality name> and <Functionality name>, which <how they divide it>. <What a solution claiming an extension adds to the capability, if any.>

<Functionalities a reader might expect here, and where each was placed instead.>

#### Core and extensions

<!--
If the specification has no extensions, replace this section with one sentence: "Every functionality is part of the core." and delete the table.

Otherwise:
- Explain the core first, and why it stands alone: what a solution that meets only the core can do, and why that makes it an instance of the Building Block
- One row per extension, matching the extensions declared in metadata.yml, with the same titles
- Adds: what a solution claiming the extension can do that the core alone cannot. Write it for a buyer deciding whether to require it
- Role served: the role the Building Block performs through the extension, and the Domain Reference Architecture that describes it. Leave empty if none
- Requires: other extensions a solution must also claim
- Explain why each extension is not core: some conformant products legitimately lack it, it is an obligation towards a domain role not every deployment has, or it depends on infrastructure not every deployment has
- Say which combinations you expect buyers to ask for
-->

The core is <what a solution that meets only the core can do, and why that is enough to make it an instance of the Building Block>.

| Extension | Adds | Functionalities | Role served | Requires |
|---|---|---|---|---|
| <Extension> | <What a solution claiming it can do that the core alone cannot> | <Functionality name> | <role>, towards <role>, in `<govstack:ra:identifier>` | <Extension, or empty> |

<Why each extension is not core, and which combinations buyers are expected to ask for.>

<!-- Functionality map: functionalities inside the boundary, actors outside it, and how each actor reaches each functionality. Draw each extension as a group inside the boundary; without extensions, drop the groups. A functionality no actor reaches, directly or through another functionality, is probably an internal mechanism. -->

```mermaid
flowchart LR
  ActorA(["<Actor><br/>(person)"])
  ActorB[["<Actor>"]]

  subgraph SUT["<Building Block name> Building Block (system under test)"]
    direction TB
    subgraph Core["Core"]
      F1["<Functionality name>"]
    end
    subgraph Ext1["<Extension> extension"]
      F2["<Functionality name>"]
    end
    F1 --> F2
  end

  ActorA -- "<interaction>" --> F1
  ActorB -- "<interaction>" --> F2
  F2 -- "<interaction>" --> ActorB
```

*Figure 2: functionality map of the <Building Block name> Building Block.*

### Actors

<!--
List every actor the Building Block interacts with: people, organisations, other systems and other Building Blocks.

- Specified where: the publication that defines the actor's behaviour (a Domain Reference Architecture, another Building Block specification, an external standard, or "Not specified"). An actor outside the boundary is never specified by this document, only its interface with the Building Block
- Use the role names of the Domain Reference Architecture where one exists
- Every actor marked Outside reappears in "Not covered" in scope.md, with its owner
- When an actor reaches the Building Block only through an extension, name the extension: "<Functionality name> (<Extension> extension)"
-->

| Actor | Kind | Boundary | Reaches the Building Block through | Specified where |
|---|---|---|---|---|
| <Actor> | <Person \| Organisation \| System \| Building Block> | <Inside \| Outside> | <Functionality name> | <`govstack:...` \| external standard \| Not specified> |

### Interfaces

<!--
List every interface that crosses the boundary of the system under test.

- Type: Service API, Consumed API, Protocol, Event, User interface, Device or File
- Every interface listed is realised by at least one requirement whose interaction field matches its type (SERVICE_API, CONSUMED_API, PROTOCOL, EVENT, USER_INTERFACE, DEVICE, FILE), and every requirement that is not INTERNAL realises an interface listed here
- Do not list interfaces inherited from the cross-functional requirements (logging, monitoring, deployment), unless this Building Block adds to the inherited contract
- Record the logical counterpart, not the Information Mediator, unless the Building Block depends on a mediation feature specifically
- Name the contract, not the technology
- A protocol defined for a domain is usually realised by an extension functionality. If a core functionality realises it, explain in "Core and extensions" why every conformant solution needs it
-->

| Interface | Counterpart | Direction | Functionality | Type | Contract defined in |
|---|---|---|---|---|---|
| <Interface name> | <Actor> | <Inbound \| Outbound \| both, described> | <Functionality name> | <Type> | <This specification, `resources/api/...` \| `govstack:...` \| external standard> |
