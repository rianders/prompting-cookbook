# Example: Interactive Vocabulary Practice

## Scenario
Students need to practice Week 1 vocabulary before moving on.

## Source files
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/2024 Spring Byrne Class Bibliography.docx`

## Weak starting prompt
```text
Make a vocabulary activity.
```

## Why the weak prompt falls short
- It does not define which vocabulary matters for this course.
- It does not say whether the activity should be a worksheet, Canvas activity, or interactive HTML.
- It gives no course framing or student-level constraint.

## Better grounded prompt
```text
You are both an instructional designer and a front-end learning activity developer.

Use the attached module materials as the primary source of truth:
- the course syllabus
- the Week 1 course framing
- the vocabulary or concepts I want students to practice
- any student-level, accessibility, Canvas, or hosting constraints I provide

Task:
Create a small interactive vocabulary practice activity that helps students confirm understanding before moving on.

Technical requirements:
- output a single self-contained HTML file
- include HTML, CSS, and JavaScript in one file
- do not use external dependencies
- include a completion or summary section students can use as a submission artifact if needed

Important constraints:
- Use course-specific terminology, not generic XR buzzwords.
- Keep the activity low-stakes and appropriate for Week 1.
- If any vocabulary list or definition is missing, mark it as [NEEDS REVIEW].

Return:
1. a short description of the activity
2. the complete self-contained HTML file
3. a note explaining how it supports the module learning objective
4. any [NEEDS REVIEW] items
```

## Expected output shape
- a small interactive matching, sorting, or recall activity
- definitions and terms tied to the course materials
- a short explanation of instructional fit

## Review notes
- Check whether the terms come from the course rather than a generic AR/VR glossary.
- Check whether the interaction type is simple enough for first-week use.
- Check whether the submission/completion artifact is actually usable in your LMS workflow.

## Why this example is useful
This example connects the hosted-activity recipe to a realistic faculty task: turning course vocabulary into a quick, low-friction practice element.
