# Example: Zero-Shot Grading vs Grounded Grading

## Scenario
An instructor wants help responding to a final reflection paper in the XR course.

## Source files
- `sources/xrcourse/final-reflection-paper-due-friday-4-slash-5.html`
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`

## Student response excerpt
```text
Our project focused on helping people notice community history that is often invisible in everyday movement through New Brunswick. I think the vulnerability we addressed was disconnection from local history and from the people affected by redevelopment. The game format made people stop, look, and connect the mural site to larger community issues.
```

## Zero-shot grading request
```text
Grade this student answer.
```

## Why the zero-shot version falls short
- It gives the model no assignment context.
- It gives the model no course goals or local framing.
- It encourages grading against generic expectations instead of course-specific ones.

## Grounded grading prompt
```text
You are helping me evaluate student work using my course materials, not general background knowledge.

Use the attached materials as the primary source of truth:
- the student response
- the final reflection assignment prompt
- the course syllabus and learning goals
- any course values or time-frame notes I provide

Task:
Evaluate this response using the assignment framing and the course-specific goals.

Important constraints:
- Base your evaluation on the supplied course materials.
- Do not grade based on general outside expectations unless they are clearly supported by the assignment or syllabus.
- If a judgment depends on rubric detail that has not been supplied, mark it as [UNCERTAIN].

Return:
1. strengths of the response
2. possible gaps or missed opportunities
3. one specific next step for revision or improvement
4. one sentence explaining how the response aligns or does not align with the course goals
5. any [UNCERTAIN] points caused by missing rubric detail
```

## Materials provided
- the final reflection prompt
- the course syllabus and learning goals
- the student response excerpt

## Expected output shape
- feedback grounded in the actual prompt and course aims
- explicit uncertainty where scoring criteria are missing
- revision advice tied to the course's social-engagement framing

## Review notes
- Check whether the feedback refers to the actual reflection prompt.
- Check whether the evaluation uses the course goals rather than a generic writing rubric.
- Check whether missing rubric criteria are flagged instead of silently assumed.

## Why this example is useful
This example shows how grounded grading still works even when the source materials are incomplete, as long as the prompt tells the model to surface uncertainty instead of inventing a rubric.
