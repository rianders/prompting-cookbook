# Example: Alt-Text Generation from Course Context

## Scenario
An instructor has a tall PNG export of math lecture notes and wants a draft alt-text description that is useful to students using screen readers.

## Source files
- `sources/math/2022-0922 Section 13 Notes.png`

## Weak starting prompt
```text
Write alt text for this image.
```

## Why the weak prompt falls short
- It does not explain the instructional purpose of the image.
- It does not tell the model whether the image is decorative, text-heavy, or central to the lesson.
- It does not warn the model to flag unreadable or uncertain details.

## Better grounded prompt
```text
You are helping me draft alt text for course materials.

Use the attached materials as the primary source of truth:
- the uploaded PNG of lecture notes
- the fact that this image comes from a math course handout
- any surrounding slide title, section heading, or instructor notes I provide

Task:
Write draft alt text that helps a student understand the instructional purpose of this image.

Important constraints:
- Base the description on what is actually visible and on the supplied course context.
- Do not invent formulas, labels, or definitions that are unreadable in the image.
- Prioritize the content a student would need in order to understand why this image appears in the lesson.
- If the image is too dense for concise alt text alone, provide a short alt text draft plus a note that a longer description is needed.
- Mark any unreadable or uncertain visual details as [UNCERTAIN].

Return:
1. concise alt text draft
2. if needed, a short longer-description draft
3. any [UNCERTAIN] details that need human review
```

## Materials provided
- the PNG image itself
- the lesson context that it is part of a math section handout
- any section title or nearby explanatory text from the instructor

## Expected output shape
- one short alt-text draft suitable for a page or LMS upload
- one optional longer description if the image is too dense
- one short review note listing formulas, labels, or text that need human confirmation

## Review notes
- Check whether the draft captures the teaching purpose, not just the visible layout.
- Check whether formulas, variable names, or labels were invented.
- If the image is a long note sheet, consider replacing the image with accessible text in addition to alt text.

## Why this example is useful
This example shows that alt text for teaching materials needs course context and uncertainty handling. Generic image-captioning is not enough for a dense instructional artifact.
