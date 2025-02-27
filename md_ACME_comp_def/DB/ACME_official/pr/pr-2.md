---
x-trestle-comp-def-rules:
  DB:
    - name: db_password_min_length
      description: Ensure min. length of password
    - name: db_password_not_reuse_min_count
      description: 'Ensure password is not reused below # count'
x-trestle-global:
  profile:
    title: ACME Inc. official controls profile.
    href: trestle://profiles/ACME_official/profile.json
x-trestle-rules-params:
  DB:
    - name: db_min_pass_len
      description: Min. password length
      options: 8, 12, 16
      rule-id: db_password_min_length
    - name: db_min_pass_reuse_count
      description: Min. password reuse count
      options: 4, 8
      rule-id: db_password_not_reuse_min_count
x-trestle-comp-def-rules-param-vals:
  # You may set new values for rule parameters by adding
  #
  # component-values:
  #   - value 1
  #   - value 2
  #
  # below a section of values:
  # The values list refers to the values as set by the components, and the component-values are the new values
  # to be placed in SetParameters of the component definition.
  #
  DB:
    - name: db_min_pass_len
      values:
        - '16'
    - name: db_min_pass_reuse_count
      values:
        - '8'
---

# pr-2 - \[Privilege Rating\] Registering exemptions to right to delete

## Control Statement

______________________________________________________________________

## What is the solution and how is it implemented?

<!-- For implementation status enter one of: implemented, partial, planned, alternative, not-applicable -->

<!-- Note that the list of rules under ### Rules: is read-only and changes will not be captured after assembly to JSON -->

<!-- Add control implementation description here for control: pr-2 -->

### Rules:

  - db_password_min_length
  - db_password_not_reuse_min_count

### Implementation Status: planned

______________________________________________________________________
