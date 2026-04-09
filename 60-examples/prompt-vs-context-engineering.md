# Example: Prompt vs Context Engineering

## Scenario
An instructor wants AI to help create a Week 1 activity for the XR and Social Engagement course.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`
- `sources/xrcourse/The Black Community in New Brunswick (1).docx`

## Prompt only
```text
Write a quiz on XR.
```

## Why prompt-only is weak
- It asks for output without defining the course context.
- It does not say whether the focus is technical XR knowledge, community history, or course framing.
- It gives the model no reason to stay within the supplied course materials.

## Context-engineered request
```text
You are helping me create a Week 1 learning activity for my course.

Use the attached materials as the primary source of truth:
- the course syllabus
- the Week 1 framing around XR and social engagement
- the local New Brunswick readings already assigned in the course
- any instructor notes about student level or course values

Task:
Create a short low-stakes activity that helps students connect introductory XR ideas to the course's local community context.

Important constraints:
- Base the activity on the supplied course materials, not on generic XR background knowledge.
- Keep the activity realistic for the first week of an introductory seminar.
- Include both conceptual understanding and local context.
- If any part of the activity depends on missing material, mark it as [NEEDS REVIEW].

Return:
1. a short activity description
2. the student prompt
3. a note explaining which sources shaped the activity
4. any [NEEDS REVIEW] items
```

## What changed
- The prompt wording is not the main upgrade.
- The main upgrade is the surrounding context: syllabus, local readings, constraints, course values, and review behavior.

## Expected output shape
- a course-specific activity rather than generic XR trivia
- explicit grounding in New Brunswick materials
- a short provenance note

## Review notes
- Check whether the output uses the local course readings rather than generic examples.
- Check whether the task fits Week 1 student readiness.
- Check whether the model flags unsupported ideas instead of silently inventing them.

## Why this example is useful
This example makes the repo's core claim concrete: better results come from better context design, not just clever wording.
