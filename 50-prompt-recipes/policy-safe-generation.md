# Prompt Recipe: Policy-Safe Generation

## Goal
Generate teaching support materials while respecting privacy and approved-tool constraints.

## Use this when
- you want AI help but need to stay within local privacy, policy, or approved-tool boundaries
- you are handling student work, course records, or institution-specific materials

## Gather these materials
- the teaching task you want completed
- the source materials needed for the task
- any local policy or departmental guidance
- approved-tool constraints
- prohibited data types or sharing restrictions
- anonymized or redacted examples if relevant

## Copy/paste prompt
```text
You are helping me complete a teaching task while staying within my institution's privacy, data-handling, and approved-tool constraints.

Use the attached materials as the primary source of truth:
- the task description
- the course materials needed for the task
- any local policy notes or approved-tool guidance I provide
- any redacted or anonymized examples I provide

Task:
Help me complete this task in a way that stays policy-safe and instructionally useful.

Important constraints:
- Do not request or rely on student-identifying information unless I explicitly confirm it is permitted.
- Do not invent institutional rules that are not present in the supplied materials.
- If the task would require restricted data or a non-approved workflow, stop and propose a safer alternative.
- Prefer redacted, summarized, or synthetic examples when those can accomplish the goal.
- Clearly mark any point where human review or a different approved tool is needed.

Return:
1. recommended safe workflow for this task
2. the draft output, if it can be produced safely from the supplied materials
3. a short list of policy or privacy risks to avoid
4. any required human-review or approved-tool handoff points
```

## Watchouts
- Do not paste identifiable student work into a tool unless the policy basis is clear.
- Do not confuse "helpful" with "allowed"; a technically possible workflow may still be out of bounds.
- Do not let the model silently substitute invented policy language for missing guidance.
- Do not assume redaction is complete if names are removed but context still identifies the student.

## Revision moves
- add the actual approved-tool guidance if the response stays too abstract
- replace raw student data with a redacted sample if the task can be demonstrated safely
- ask for a safer fallback workflow if the requested task crosses a policy line
- ask the model to separate "can do now" from "requires approved environment" if the answer mixes them

## See also
- `20-constraints/policy-aware-prompting.md`
- `20-constraints/institutional-requirements.md`
- `COMMON-MISTAKES-AND-WARNINGS.md`
- `60-examples/policy-safe-generation-example.md`
