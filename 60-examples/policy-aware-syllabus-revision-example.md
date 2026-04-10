# Example: Policy-Aware Syllabus Revision

## Scenario
An instructor is updating the Social Engagement in XR syllabus from the Fall 2024 version to the Spring 2026 version. They want to check that required institutional elements are present, that policy language has not been silently dropped between versions, and that the accessibility statement reflects current expectations. They do not want the model to invent policy language — only to surface what is present, what changed, and what may be missing.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/2024FA_ Social Engagement in XR (Extended Reality).docx`

## Risky starting prompt
```text
Update my syllabus with the right policies.
```

## Why the risky prompt falls short
- It invites the model to invent policy language that may not reflect actual institutional requirements.
- It does not define which version is the source of truth or what changed between versions.
- It does not tell the model what to do when a required element is missing from both versions.

## Better grounded prompt
```text
You are helping me revise my course syllabus using two existing syllabus versions as source documents.

Use the attached materials as the primary source of truth:
- the Spring 2026 syllabus draft (current version to be revised)
- the Fall 2024 syllabus (previous version for comparison only)

Task:
Compare the two versions and revise the Spring 2026 syllabus so that required and recommended policy elements are present, clearly stated, and consistent with the supplied documents.

Important constraints:
- Treat the Spring 2026 syllabus as the main document. The Fall 2024 version is a comparison reference only — do not restore removed content without flagging it.
- Do not invent Rutgers, school, or department policies that are not present in either document.
- Pay specific attention to the following policy areas:
  - accessibility statement (WCAG 2.1+ or equivalent; disability accommodation language)
  - academic integrity statement
  - AI/technology use policy
  - late work and attendance policy
  - required contact and office hours information
- If a required or recommended element appears in the Fall 2024 version but is missing from the Spring 2026 version, flag it clearly rather than silently restoring it.
- If a required element appears to be missing from both versions, mark it as [NEEDS CONFIRMATION] and do not invent replacement language.

Return:
1. revised Spring 2026 syllabus draft with tracked policy additions or changes noted inline
2. a list of policy sections added or revised, with a note on which source document supported each change
3. a checklist of elements that appear to be missing or that need instructor confirmation
4. any [NEEDS CONFIRMATION] items that require the instructor to supply actual institutional policy text
```

## Materials provided
- the Spring 2026 syllabus as the current working draft
- the Fall 2024 syllabus as a historical comparison document

## Expected output shape
- a revised syllabus draft that is clearly bounded to the supplied materials
- a visible audit trail — what changed, where it came from
- a clear list of what the model could not resolve without more information

## Review notes
- Verify that every added policy statement is traceable to one of the two supplied documents.
- Check whether the accessibility statement names a specific standard. If WCAG 2.1+ is not mentioned, this is a gap to flag.
- Do not let the model merge older policy language into the new draft without explicit instructor review — some changes between versions may have been intentional.
- Any [NEEDS CONFIRMATION] item should go to the instructor or the department for actual policy text before the syllabus is distributed.

## Why this example is useful
This example is distinct from the policy-safe generation example in two ways: it works from two syllabus versions rather than one, and its goal is revision and auditing rather than new content generation. The comparison-without-merging pattern is useful any time an instructor is updating documents across semesters and needs to know what was dropped, what changed, and what might now be out of compliance.
