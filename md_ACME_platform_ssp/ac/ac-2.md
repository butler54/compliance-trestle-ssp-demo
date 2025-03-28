---
x-trestle-comp-def-rules:
  DB:
    - name: db_authorized_users_only
      description: Ensure only authorized users can access
x-trestle-set-params:
  # You may set values for parameters in the assembled SSP by adding
  #
  # ssp-values:
  #   - value 1
  #   - value 2
  #
  # below a section of values:
  # The values list refers to the values in the resolved profile catalog, and the ssp-values represent new values
  # to be placed in SetParameters of the SSP.
  #
  ac-2_prm_1:
    values:
      - privileged
  ac-2_prm_2:
    values:
      - privileged
  ac-2_prm_3:
    values:
      - standard operations
  ac-2_prm_4:
    values:
      - daily
x-trestle-evidence:
  named-evidence: location
x-trestle-dependent-on:
  - control-id:
    profile:
reviewed-by:
  - named:
    date:
x-trestle-fedramp-props:
  control-origination:
    - Service provider Corporate
    - Service provider System Specific
    - Service Provider Hybrid (Corporate and System Specific)
    - Configured by Customer (Customer System Specific)
    - Provided by Customer (Customer System Specific)
    - Shared (Service Provider and Customer Responsibility)
    - Inherited from pre-existing FedRAMP Authorization [Enter text here], Date of
      Authorization
  implementation-status:
    - Implemented
    - Partially implemented
    - Planned
    - Alternative implementation
    - Not Applicable
  responsible-roles:
x-trestle-global:
  profile:
    title: ACME Inc. internal controls profile.
    href: trestle://profiles/ACME_int_guidance/profile.json
  sort-id: ac-02
x-trestle-add-props: []
  # Add or modify control properties here
  # Properties may be at the control or part level
  # Add control level properties like this:
  #   - name: ac1_new_prop
  #     value: new property value
  #
  # Add properties to a statement part like this, where "b." is the label of the target statement part
  #   - name: ac1_new_prop
  #     value: new property value
  #     smt-part: b.
  #
---

# ac-2 - \[Access Control\] Account Management

## Control Statement

The organization:

- \[a.\] Identifies and selects the following types of information system accounts to support organizational missions/business functions: [privileged];

- \[b.\] Assigns account managers for information system accounts;

- \[c.\] Establishes conditions for group and role membership;

- \[d.\] Specifies authorized users of the information system, group and role membership, and access authorizations (i.e., privileges) and other attributes (as required) for each account;

- \[e.\] Requires approvals by [organization-defined personnel or roles] for requests to create information system accounts;

- \[f.\] Creates, enables, modifies, disables, and removes information system accounts in accordance with [standard operations];

- \[g.\] Monitors the use of information system accounts;

- \[h.\] Notifies account managers:

  - \[1.\] When accounts are no longer required;
  - \[2.\] When users are terminated or transferred; and
  - \[3.\] When individual information system usage or need-to-know changes;

- \[i.\] Authorizes access to the information system based on:

  - \[1.\] A valid access authorization;
  - \[2.\] Intended system usage; and
  - \[3.\] Other attributes as required by the organization or associated missions/business functions;

- \[j.\] Reviews accounts for compliance with account management requirements [daily]; and

- \[k.\] Establishes a process for reissuing shared/group account credentials (if deployed) when individuals are removed from the group.

## Control Objective

Determine if the organization:

- \[AC-2(a)\]

  - \[AC-2(a)[1]\] defines information system account types to be identified and selected to support organizational missions/business functions;
  - \[AC-2(a)[2]\] identifies and selects organization-defined information system account types to support organizational missions/business functions;

- \[AC-2(b)\] assigns account managers for information system accounts;

- \[AC-2(c)\] establishes conditions for group and role membership;

- \[AC-2(d)\] specifies for each account (as required):

  - \[AC-2(d)[1]\] authorized users of the information system;
  - \[AC-2(d)[2]\] group and role membership;
  - \[AC-2(d)[3]\] access authorizations (i.e., privileges);
  - \[AC-2(d)[4]\] other attributes;

- \[AC-2(e)\]

  - \[AC-2(e)[1]\] defines personnel or roles required to approve requests to create information system accounts;
  - \[AC-2(e)[2]\] requires approvals by organization-defined personnel or roles for requests to create information system accounts;

- \[AC-2(f)\]

  - \[AC-2(f)[1]\] defines procedures or conditions to:

    - \[AC-2(f)[1][a]\] create information system accounts;
    - \[AC-2(f)[1][b]\] enable information system accounts;
    - \[AC-2(f)[1][c]\] modify information system accounts;
    - \[AC-2(f)[1][d]\] disable information system accounts;
    - \[AC-2(f)[1][e]\] remove information system accounts;

  - \[AC-2(f)[2]\] in accordance with organization-defined procedures or conditions:

    - \[AC-2(f)[2][a]\] creates information system accounts;
    - \[AC-2(f)[2][b]\] enables information system accounts;
    - \[AC-2(f)[2][c]\] modifies information system accounts;
    - \[AC-2(f)[2][d]\] disables information system accounts;
    - \[AC-2(f)[2][e]\] removes information system accounts;

- \[AC-2(g)\] monitors the use of information system accounts;

- \[AC-2(h)\] notifies account managers:

  - \[AC-2(h)(1)\] when accounts are no longer required;
  - \[AC-2(h)(2)\] when users are terminated or transferred;
  - \[AC-2(h)(3)\] when individual information system usage or need to know changes;

- \[AC-2(i)\] authorizes access to the information system based on;

  - \[AC-2(i)(1)\] a valid access authorization;
  - \[AC-2(i)(2)\] intended system usage;
  - \[AC-2(i)(3)\] other attributes as required by the organization or associated missions/business functions;

- \[AC-2(j)\]

  - \[AC-2(j)[1]\] defines the frequency to review accounts for compliance with account management requirements;
  - \[AC-2(j)[2]\] reviews accounts for compliance with account management requirements with the organization-defined frequency; and

- \[AC-2(k)\] establishes a process for reissuing shared/group account credentials (if deployed) when individuals are removed from the group.

## Control guidance

Information system account types include, for example, individual, shared, group, system, guest/anonymous, emergency, developer/manufacturer/vendor, temporary, and service. Some of the account management requirements listed above can be implemented by organizational information systems. The identification of authorized users of the information system and the specification of access privileges reflects the requirements in other security controls in the security plan. Users requiring administrative privileges on information system accounts receive additional scrutiny by appropriate organizational personnel (e.g., system owner, mission/business owner, or chief information security officer) responsible for approving such accounts and privileged access. Organizations may choose to define access privileges or other attributes by account, by type of account, or a combination of both. Other attributes required for authorizing access include, for example, restrictions on time-of-day, day-of-week, and point-of-origin. In defining other account attributes, organizations consider system-related requirements (e.g., scheduled maintenance, system upgrades) and mission/business requirements, (e.g., time zone differences, customer requirements, remote access to support travel requirements). Failure to consider these factors could affect information system availability. Temporary and emergency accounts are accounts intended for short-term use. Organizations establish temporary accounts as a part of normal account activation procedures when there is a need for short-term accounts without the demand for immediacy in account activation. Organizations establish emergency accounts in response to crisis situations and with the need for rapid account activation. Therefore, emergency account activation may bypass normal account authorization processes. Emergency and temporary accounts are not to be confused with infrequently used accounts (e.g., local logon accounts used for special tasks defined by organizations or when network resources are unavailable). Such accounts remain available and are not subject to automatic disabling or removal dates. Conditions for disabling or deactivating accounts include, for example: (i) when shared/group, emergency, or temporary accounts are no longer required; or (ii) when individuals are transferred or terminated. Some types of information system accounts may require specialized training.

## Control acme_guidance

Access control documentation should be at one centrally managed intranet site that is consistent across the corporation. Website should be indexed in intranet search engine.

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

### This System

This system implemented bananas.

#### Implementation Status: implemented

______________________________________________________________________

## Implementation for part d.

### DB

Implement well for component DB and part d.

#### Rules:

  - db_authorized_users_only

#### Implementation Status: partial

______________________________________________________________________
