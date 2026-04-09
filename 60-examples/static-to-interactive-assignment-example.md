# Example: Converting a Static Assignment into an Interactive Activity

## Scenario
An instructor wants to redesign a five-paragraph community research assignment into a more scaffolded activity without losing the original course goals.

## Source files
- `sources/xrcourse/check-in-1-community-research-due-before-class-on-2-slash-7.html`
- `sources/xrcourse/Spring 2026_ Social Engagement in XR (Extended Reality).docx`
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`
- `sources/xrcourse/The Black Community in New Brunswick (1).docx`

## Original assignment
The existing assignment asks student groups to submit a 750-1000 word five-paragraph essay explaining the project's community of benefit, user audience, desired impact, and measures of success.

## Weak starting prompt
```text
Turn this assignment into something interactive.
```

## Why the weak prompt falls short
- It does not preserve the original learning purpose.
- It does not tell the model what sources students are supposed to use.
- It does not define whether the result should fit Canvas, class discussion, or a custom activity.

## Better grounded prompt
```text
You are helping me redesign a traditional assignment into a more interactive learning activity.

Use the attached materials as the primary source of truth:
- the current Check-In 1 assignment prompt
- the course syllabus and learning goals
- the community context readings on Latino migration and the Black community in New Brunswick
- any Canvas or delivery constraints I provide

Task:
Redesign this assignment so students get more structure, interaction, and feedback opportunities while still meeting the original course goals.

Important constraints:
- Preserve the core purpose of the assignment: students should still identify community of benefit, intended audience, desired impact, and measures of success.
- Keep the redesign realistic for a course module or Canvas workflow.
- Do not add outside research requirements beyond the supplied materials unless clearly marked optional.
- Avoid cosmetic interactivity that does not improve learning.
- Mark any platform assumptions as [NEEDS REVIEW].

Return:
1. a short summary of the original assignment purpose
2. a redesigned interactive version
3. a step-by-step student flow
4. a note explaining how the redesign preserves the original learning goals
5. any [NEEDS REVIEW] implementation questions
```

## Materials provided
- the original Check-In 1 assignment prompt
- syllabus framing for course goals and schedule
- local community readings already used by the course
- Canvas or hosting constraints if relevant

## Expected output shape
- a staged activity with checkpoints rather than one single submission
- a student workflow that could map to a Canvas module
- a note tying each stage back to the original assignment expectations

## Review notes
- Check that the redesigned activity still requires students to reason about community benefit, audience, impact, and success metrics.
- Check that the new structure adds support and sequence rather than lowering rigor.
- Check that the activity uses the course's local New Brunswick materials rather than generic examples.

## Why this example is useful
This example shows how context engineering can convert a static written assignment into a guided learning sequence without losing course specificity or assessment intent.
