# Example: Bare vs Context-Rich Prompt

## Scenario
An instructor wants a Week 1 quiz for the XR and Social Engagement course.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`
- `sources/xrcourse/The Black Community in New Brunswick (1).docx`

## Bare prompt
```text
Write a quiz.
```

## Why the bare prompt falls short
- It does not say what students should learn in Week 1.
- It does not say whether the quiz should focus on XR concepts, local community context, or both.
- It does not tell the model what course materials to use.

## Context-rich prompt
```text
You are helping me create a low-stakes Week 1 quiz for my course.

Use the attached materials as the primary source of truth:
- the course syllabus
- the Week 1 course framing around XR and social engagement
- the local background readings on Latino migration and the Black community in New Brunswick

Task:
Create a short low-stakes quiz that checks whether students understand the basic course framing for Week 1.

Important constraints:
- Base the quiz on the supplied course materials, not on generic XR trivia.
- Include both course-concept understanding and awareness of the local New Brunswick context.
- Keep the quiz appropriate for an introductory first week.
- If a question would require material not clearly present in the sources, omit it or mark it as [NEEDS REVIEW].

Return:
1. a quiz title
2. 5 to 7 questions
3. an answer key
4. one short note explaining which course materials shaped the quiz
```

## Materials provided
- syllabus framing for the course
- local context readings on New Brunswick communities
- the Week 1 goal of orienting students to XR in a community-engaged context

## Expected output shape
- a short introductory quiz
- questions tied to course framing rather than generic background knowledge
- a brief provenance note

## Review notes
- Check whether the quiz actually reflects Week 1 materials rather than general XR facts.
- Check whether the local New Brunswick context appears in a meaningful way.
- Check whether the difficulty level fits an introductory seminar.

## Why this example is useful
This example shows the central distinction the repo is trying to teach: changing the wording alone is less important than supplying the right context, boundaries, and source materials.
