# Example: Rubric Generation

## Scenario
An instructor needs a rubric for the final reflection paper in the Social Engagement in XR course. The paper asks students to reflect on their project's community impact, but no rubric currently exists. The instructor wants criteria that are actually tied to the course's social-engagement framing, not a generic writing rubric.

## Source files
- `sources/xrcourse/final-reflection-paper-due-friday-4-slash-5.html`
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`

## Weak starting prompt
```text
Create a rubric for this paper.
```

## Why the weak prompt falls short
- It does not tell the model what the paper is actually asking students to do.
- It produces criteria for generic academic writing rather than this assignment's community-engagement goals.
- It does not connect the rubric to the course's specific learning outcomes.

## Better grounded prompt
```text
You are an instructional design assistant helping me create a rubric.

Use the attached materials as the primary source of truth:
- the final reflection paper assignment prompt
- the course syllabus and learning goals for Social Engagement in XR

Task:
Create a rubric aligned to the learning objectives and the purpose of this final reflection assignment.

Requirements:
- Use these performance levels: Excellent, Proficient, Developing, Beginning
- Build criteria directly from the assignment prompt and course goals — do not use generic academic writing criteria unless they are explicitly relevant to this assignment
- Criteria should reflect the course's emphasis on community benefit, social engagement, and the student's ability to connect their XR project to real community impact
- Include 4 to 6 criteria total

Important constraints:
- Do not invent assignment requirements that are not present in the supplied prompt.
- If a criterion depends on rubric details that are not clearly supported by the materials, mark it as [NEEDS REVIEW].
- Keep descriptor language specific to this assignment rather than generic.

Return:
1. rubric title
2. 4 to 6 criteria with names and short descriptions
3. performance descriptors for each criterion at each level (Excellent, Proficient, Developing, Beginning)
4. one short note explaining how the rubric connects to the course learning objectives
5. any [NEEDS REVIEW] items
```

## Materials provided
- the final reflection paper prompt, which asks students to reflect on community of benefit, intended audience, desired impact, and measures of success
- the course syllabus framing social engagement as central to the XR project work

## Expected output shape
- a rubric with criteria drawn from the assignment prompt, not from generic writing expectations
- descriptor language that distinguishes levels by degree of community-specific reasoning, not just writing quality
- a clear connection between each criterion and the course goals

## Review notes
- Check whether the criteria name things the assignment actually asks for — community of benefit, impact, audience — rather than generic elements like "thesis" or "transitions."
- Check whether the performance levels are distinguishable from one another; "Excellent" and "Proficient" should not describe the same behavior.
- Check whether the rubric could be shared with students before they write — if not, revise for transparency.
- If the rubric relies on details not in the supplied prompt, those items should be marked [NEEDS REVIEW].

## Why this example is useful
This example shows how rubric generation requires the assignment prompt and the course goals together. Without both, the model defaults to a generic writing rubric that does not reflect the course's actual values or expectations.
