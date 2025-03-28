---
x-trestle-set-params:
    # This section contains the parameters that are part of this control.
  # Each parameter has properties. Only the profile-values and display-name properties are editable.
  # The other properties are informational.
  #
  # The values property for a parameter represents values inherited from the OSCAL catalog.
  # To override the catalog settings, use bullets under profile-values as shown below:
  #
  #   profile-values:
  #     - value 1
  #     - value 2
  #
  # If the "- <REPLACE_ME>" placeholder appears under profile-values, it is the same as if
  # the profile-values property were left empty.
  #
  # Some parameters may show an aggregates property which lists other parameters. This means
  # the parameter value is made up of the values from the other parameters. For parameters
  # that aggregate, profile-values is not applicable.
  #
  # Property param-value-origin is meant for putting the origin from where that parameter comes from.
  # In order to be changed in the current profile, profile-param-value-origin property will be displayed with
  # the placeholder "<REPLACE_ME>" for you to be replaced. If a parameter already has a param-value-origin
  # coming from an inherited profile, do no change this value, instead use profile-param-value-origin as follows:
  #
  #    param-value-origin: DO NOT REPLACE - this is the original value
  #    profile-param-value-origin: <REPLACE_ME> - replace the new value required HERE
  #
  ac-2_prm_1:
    values:
      - privileged
  ac-2_prm_2:
    values:
  ac-2_prm_3:
    values:
      - standard operations
  ac-2_prm_4:
    values:
      - daily
x-trestle-global:
  profile:
    title: ACME Inc. internal controls profile.
  sort-id: ac-02
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
---

# ac-2 - \[Access Control\] Account Management

## Control Statement

The organization:

- \[a.\] Identifies and selects the following types of information system accounts to support organizational missions/business functions: {{ insert: param, ac-2_prm_1 }};

- \[b.\] Assigns account managers for information system accounts;

- \[c.\] Establishes conditions for group and role membership;

- \[d.\] Specifies authorized users of the information system, group and role membership, and access authorizations (i.e., privileges) and other attributes (as required) for each account;

- \[e.\] Requires approvals by {{ insert: param, ac-2_prm_2 }} for requests to create information system accounts;

- \[f.\] Creates, enables, modifies, disables, and removes information system accounts in accordance with {{ insert: param, ac-2_prm_3 }};

- \[g.\] Monitors the use of information system accounts;

- \[h.\] Notifies account managers:

  - \[1.\] When accounts are no longer required;
  - \[2.\] When users are terminated or transferred; and
  - \[3.\] When individual information system usage or need-to-know changes;

- \[i.\] Authorizes access to the information system based on:

  - \[1.\] A valid access authorization;
  - \[2.\] Intended system usage; and
  - \[3.\] Other attributes as required by the organization or associated missions/business functions;

- \[j.\] Reviews accounts for compliance with account management requirements {{ insert: param, ac-2_prm_4 }}; and

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

# Editable Content

<!-- Make additions and edits below -->
<!-- The above represents the contents of the control as received by the profile, prior to additions. -->
<!-- If the profile makes additions to the control, they will appear below. -->
<!-- The above markdown may not be edited but you may edit the content below, and/or introduce new additions to be made by the profile. -->
<!-- If there is a yaml header at the top, parameter values may be edited. Use --set-parameters to incorporate the changes during assembly. -->
<!-- The content here will then replace what is in the profile for this control, after running profile-assemble. -->
<!-- The current profile has no added parts for this control, but you may add new ones here. -->
<!-- Each addition must have a heading either of the form ## Control my_addition_name -->
<!-- or ## Part a. (where the a. refers to one of the control statement labels.) -->
<!-- "## Control" parts are new parts added after the statement part. -->
<!-- "## Part" parts are new parts added into the top-level statement part with that label. -->
<!-- Subparts may be added with nested hash levels of the form ### My Subpart Name -->
<!-- underneath the parent ## Control or ## Part being added -->
<!-- See https://oscal-compass.github.io/compliance-trestle/tutorials/ssp_profile_catalog_authoring/ssp_profile_catalog_authoring for guidance. -->
