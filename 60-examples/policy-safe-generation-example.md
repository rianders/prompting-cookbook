# Example: Policy-Safe Teaching Support Workflow

## Scenario
An instructor wants AI help revising a syllabus and generating support materials, but needs to stay within institutional policy boundaries and avoid invented policy language.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/2024FA_ Social Engagement in XR (Extended Reality).docx`

## Risky starting prompt
```text
Rewrite my syllabus, add the Rutgers policies I need, and create anything else that should be included.
```

## Why the risky prompt falls short
- It invites the model to invent policy language.
- It does not define which syllabus version is the source of truth.
- It does not tell the model what to do when local policy guidance is missing.

## Better grounded prompt
```text
You are helping me revise course materials while staying within my institution's policy and approved-tool constraints.

Use the attached materials as the primary source of truth:
- my current Spring 2026 syllabus draft
- the earlier syllabus version for comparison
- any local policy notes or approved-tool guidance I provide

Task:
Help me identify policy-sensitive syllabus sections and draft revisions without inventing institutional requirements.

Important constraints:
- Do not invent Rutgers, school, or department policies that are not present in the supplied materials.
- Treat the Spring 2026 syllabus as the main source document unless I say otherwise.
- Use the earlier syllabus only as a comparison aid, not as a replacement authority.
- If a required section appears to be missing but is not documented in the materials, mark it as [NEEDS CONFIRMATION].
- If part of the task would require a different approved environment or human review, say so explicitly.

Return:
1. a list of policy-sensitive sections in the syllabus
2. draft revision language grounded in the supplied materials
3. any [NEEDS CONFIRMATION] items
4. a short note explaining which source document shaped each major revision
```

## Materials provided
- the Spring 2026 syllabus as the current draft
- the earlier syllabus as comparison context
- any institutional guidance the instructor is prepared to supply

## Expected output shape
- a clearly bounded revision draft
- a checklist of uncertain or missing items
- an explicit distinction between supported revisions and unsupported guesses

## Review notes
- Verify that every added policy statement appears in the provided materials.
- Check that the model did not merge older syllabus language into the new draft without justification.
- Confirm that any unresolved requirements are flagged instead of silently filled in.

## Why this example is useful
This example shows how to use AI for policy-sensitive course work without turning the model into an unauthorized source of institutional rules.
