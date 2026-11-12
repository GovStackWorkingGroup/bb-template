---
title: functionality name
description: |
   <description from the business PoV>
realises: [] # ids of capabilities declared in metadata.yml. At least one
conformance: CORE # Options: [CORE, EXTENSION]. CORE: every conformant solution meets it. EXTENSION: only solutions that claim its extension
extension: # id of an extension declared in metadata.yml. Only when conformance is EXTENSION
requirements:
  - id: '1'
    status: DRAFT # [DRAFT, WITHDRAWN, CANDIDATE, ACCEPTED, PUBLISHED, DEPRECATED]
    level: RECOMMENDED # [RECOMMENDED, REQUIRED]
    observability: # [OBSERVABLE, AUDITABLE]
    mutability: # [IMMUTABLE, EXTENSIBLE]
    interaction: # [SERVICE_API, CONSUMED_API, PROTOCOL, EVENT, USER_INTERFACE, DEVICE, FILE, INTERNAL]. Where the requirement is exercised: across which boundary, or at none
    contract: # where the contract is defined, when it is defined elsewhere. Required for CONSUMED_API, PROTOCOL, DEVICE and FILE when not defined in this specification
    statement: <The requirement statement is a single sentence that describes the requirement in a clear and concise manner.>
    documentation: >
      This is the text description of the requirement and can span multiple
      lines and even contain *markdown* _formatting_.
    api_operation_id: # operation in resources/api/. Required when interaction is SERVICE_API
    test: 
---

<!-- Here goes the description and rendering of the functionality that goes into the technical sections -->
# Workflows
# Data structure