# Example: Canvas Translation

## Scenario
An instructor wants to translate the Check-In 1 community research assignment into a small Canvas-ready module.

## Source files
- `sources/xrcourse/check-in-1-community-research-due-before-class-on-2-slash-7.html`
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`
- `sources/xrcourse/The Black Community in New Brunswick (1).docx`

## Weak starting prompt
```text
Put this assignment into Canvas.
```

## Why the weak prompt falls short
- It does not define the learning flow.
- It does not say which course materials should appear alongside the assignment.
- It does not specify what kinds of Canvas objects are needed.

## Better grounded prompt
```text
You are helping me translate an assignment into a Canvas-ready learning module.

Use the attached materials as the primary source of truth:
- the Check-In 1 assignment prompt
- the course syllabus and learning goals
- the local New Brunswick context readings students are expected to use
- any Canvas or accessibility constraints I provide

Task:
Convert this assignment into a small Canvas module that gives students enough structure to complete the work successfully.

Important constraints:
- Preserve the original assignment purpose and required writing task.
- Use the supplied local readings as the main supporting materials.
- Organize the result into realistic Canvas objects rather than generic LMS advice.
- Keep the module low-friction and realistic for a single course week.
- Mark any platform assumptions as [NEEDS REVIEW].

Return:
1. a recommended Canvas module structure
2. page-by-page or item-by-item Canvas objects
3. short draft text for each object
4. any [NEEDS REVIEW] implementation questions
```

## Likely Canvas objects
- overview page
- content/materials page
- activity instructions page
- submission assignment
- optional discussion or check-in page

## Expected output shape
- a sequence of concrete Canvas items
- short instructor-ready text blocks
- a clear connection between readings, instructions, and submission

## Review notes
- Check whether the Canvas flow adds scaffolding rather than just reformatting the assignment.
- Check whether the module uses the local course readings explicitly.
- Check whether the translation preserves the assignment's core writing expectations.

## Why this example is useful
This example turns a vague “put it in Canvas” request into a context-rich module design task with clear inputs, boundaries, and implementation assumptions.
