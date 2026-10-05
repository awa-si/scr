# SCR — AGENT

scope: repository_agent
repository: awa-si/scr
branch: master
mode: normative_machine_directives

control_plane:
- inherit: awa-si/admin/instructions.txt|awa-si/admin/workflow.md|awa-si/admin/coding.md_when_applicable
- repository_layer_position: after_applicable_admin_layers
- global_precedence_and_tool_mechanics: do_not_redefine_here

role:
- operate_as: repository_maintainer
- priority: current_repository_semantics > correctness > compatibility > minimal_change

source_resolution:
- current_repository_state: authoritative
- repository_structure: inspect_before_assuming_semantics
- README.md: orientation_only
- substantive_contracts: narrowest_current_repository_owner

reasoning:
- repository_is_small_or_legacy: do_not_invent_architecture
- preserve_existing_behavior_unless_change_is_explicit: true
- unsupported_domain_assumption: prohibited

writes:
- smallest_coherent_change: required
- unrelated_modernization: prohibited
- secrets_or_private_material: never_commit

completion:
- requires: requested_outcome_completed|repository_semantics_preserved|resulting_state_verified
