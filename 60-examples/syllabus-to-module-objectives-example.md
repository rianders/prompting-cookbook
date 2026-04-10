# Example: Syllabus to Module Objectives

## Scenario
An instructor has a full course syllabus for Social Engagement in XR and wants to generate clear, measurable module-level objectives for Week 3, when students begin their first community research task.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`

## Weak starting prompt
```text
Write learning objectives for Week 3.
```

## Why the weak prompt falls short
- It does not say what Week 3 is supposed to accomplish in this course.
- It gives the model no information about the community-engagement framing central to the course.
- It produces generic objectives that could belong to any XR or social science course.

## Better grounded prompt
```text
You are an instructional design assistant.

Use the attached syllabus and course materials as the primary source of truth:
- the Spring 2026 Social Engagement in XR syllabus
- any schedule, topic list, or weekly overview present in the document

Task:
Generate module-level learning objectives for Week 3 of this course.

Important constraints:
- Stay within the scope of the course materials as written.
- Do not invent course goals or themes that are not supported by the syllabus.
- Objectives should be measurable — use action verbs (identify, describe, compare, apply, analyze).
- Objectives should reflect both the XR component and the social engagement framing of the course, not just one side.
- If Week 3 coverage is ambiguous or not clearly described in the syllabus, mark it as [NEEDS REVIEW].
- Do not assume prior knowledge or technology access beyond what the syllabus describes.

Return:
1. module title for Week 3
2. short module purpose (2-3 sentences)
3. 3 to 5 learning objectives using measurable action verbs
4. one short note explaining how each objective connects to the syllabus
5. any [NEEDS REVIEW] items where the syllabus was ambiguous

Selected week or unit: Week 3
```

## Materials provided
- the full course syllabus including weekly topics, readings, and assignment schedule
- the course framing around local community engagement in New Brunswick

## Expected output shape
- a module title and purpose grounded in the course's community-engagement theme
- objectives that are specific enough to guide an assessment or activity design
- a clear note tying each objective back to syllabus language

## Review notes
- Check whether the objectives are actually measurable — reject vague language like "understand" or "appreciate."
- Check whether both XR and social engagement are represented, not just one dimension.
- Check whether the objectives stay within the scope of Week 3 rather than blending in the full semester.
- If objectives reference community readings or field activities, confirm those are scheduled in Week 3.

## Why this example is useful
This example shows how a full course syllabus can serve as the sole source document for objective generation — no extra instructions needed if the syllabus is supplied and the prompt specifies the target week clearly.
