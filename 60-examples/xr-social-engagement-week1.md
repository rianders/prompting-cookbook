# Example: XR and Social Engagement Week 1

## Scenario
An instructor is designing the first week of the XR and Social Engagement course and wants AI help generating course-aligned materials without losing the local community framing.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/2024-01-24 Mural Location.pdf`
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`
- `sources/xrcourse/The Black Community in New Brunswick (1).docx`

## Core Week 1 elements
- orient students to XR
- define social engagement in course context
- use community materials from New Brunswick
- introduce murals and related local resources
- emphasize phone-based or hybrid immersive experiences

## Weak starting prompt
```text
Create Week 1 materials for my XR course.
```

## Why the weak prompt falls short
- It does not define what Week 1 is supposed to accomplish.
- It does not anchor the output in local community materials.
- It does not tell the model which technologies, themes, or delivery constraints matter.

## Better grounded prompt
```text
You are helping me design Week 1 materials for a course on Social Engagement in XR.

Use the attached materials as the primary source of truth:
- the course syllabus
- the local New Brunswick readings
- the mural/location materials
- any instructor notes about delivery format, student level, and technology constraints

Task:
Draft a Week 1 module outline that introduces students to XR through the course's local community-engagement framing.

Important constraints:
- Stay within the themes and scope supported by the supplied course materials.
- Keep the first week introductory and accessible to students with limited technical background.
- Use local New Brunswick context as course content, not as decorative background.
- If a recommendation depends on missing readings, images, or activity constraints, mark it as [NEEDS REVIEW].

Return:
1. a short Week 1 module overview
2. 3 to 5 learning objectives
3. one low-stakes activity idea
4. one short note explaining how the local materials shape the week
5. any [NEEDS REVIEW] items
```

## Expected output shape
- an introductory week plan grounded in the syllabus
- module objectives tied to local course materials
- a low-stakes activity that prepares students for later work

## Review notes
- Check whether the week design is genuinely grounded in local materials.
- Check whether the technical expectations are realistic for Week 1.
- Check whether the activity and objectives reflect both XR and social engagement, not just one side.

## Why this example is useful
This example shows how multiple source types can work together: syllabus, local readings, and visual/community materials all contribute to a grounded Week 1 design.
