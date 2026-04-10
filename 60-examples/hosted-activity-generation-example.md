# Example: Hosted Activity Generation

## Scenario
An Italian language instructor wants to convert part of an advanced lesson into a self-contained interactive HTML activity that students can access through Canvas. The activity should let students practice key grammar or vocabulary from the lesson, include a submission artifact, and be fully keyboard-accessible per WCAG 2.1+.

## Source files
- `sources/italian/advanced_lesson.pdf`

## Weak starting prompt
```text
Make an interactive version of this lesson.
```

## Why the weak prompt falls short
- It does not define what "interactive" means for a language activity — flashcards, fill-in-the-blank, multiple choice, drag-and-drop, or something else.
- It does not include accessibility requirements, so the generated HTML may fail keyboard navigation or color contrast.
- It does not specify that the file must be self-contained for Canvas hosting.

## Better grounded prompt
```text
You are both an instructional designer and a front-end learning activity developer.

Use the attached module materials as the primary source of truth:
- the advanced Italian lesson PDF
- the delivery context I describe below

Delivery context:
- Course level: advanced Italian language
- Format: self-contained HTML file embedded in Canvas or hosted externally
- Students may use keyboard navigation, screen readers, or mobile devices

Task:
Create a small interactive activity that helps students practice key grammar or vocabulary from the supplied Italian lesson. Choose the activity type (e.g., fill-in-the-blank, matching, short-answer review) based on what the lesson content best supports.

Technical requirements:
- output a single self-contained HTML file
- include HTML, CSS, and JavaScript in one file
- do not use external dependencies or CDN links
- include a completion or summary section students can copy and submit as evidence of participation

Accessibility requirements (WCAG 2.1+):
- use semantic HTML elements (headings, lists, buttons, labels) rather than styled divs
- all interactive elements must be reachable and operable by keyboard alone (Tab, Enter, Space)
- associate all form inputs and interactive controls with visible labels using <label> or aria-label
- do not use color as the only means of indicating correct answers, errors, or required fields
- text and background color combinations must meet a contrast ratio of at least 4.5:1
- do not autoplay audio or video
- if the activity includes any images from the lesson, include appropriate alt text

Language requirements:
- use vocabulary and grammar structures drawn from the supplied lesson, not from generic Italian language resources
- if the lesson content is unclear or insufficient to build a complete activity, mark those items as [NEEDS REVIEW]

Return:
1. a short description of the activity type and what it practices
2. the complete self-contained HTML file
3. a note explaining how the activity supports the lesson's learning objective
4. a short WCAG 2.1+ checklist confirming which accessibility requirements are met
5. any [NEEDS REVIEW] items where lesson content was ambiguous
```

## Materials provided
- the advanced Italian lesson PDF as the primary content source
- delivery context: Canvas-hosted HTML, advanced language students, keyboard and screen reader access

## Expected output shape
- a single HTML file that opens in a browser with no internet connection required
- activity content drawn from the actual lesson vocabulary and grammar, not generic Italian
- a completion section students can use as a submission artifact
- a WCAG 2.1+ checklist attached to the output

## Review notes
- Open the HTML file in a browser and test with keyboard alone before sharing with students — Tab through every interactive element and confirm each is reachable.
- Verify color contrast with a contrast checker tool (WebAIM Contrast Checker or similar) — the model cannot measure contrast ratios reliably.
- Check that the completion section captures enough information to be useful as a submission artifact in your LMS.
- If any vocabulary or grammar in the activity does not appear in the lesson, flag it as invented content.

## Why this example is useful
This is the second example in the cookbook to use the Italian course source materials, and the first to generate a digital artifact from them. It demonstrates that the hosted activity recipe works across disciplines — language courses have the same hosting and accessibility constraints as XR or STEM courses — and that WCAG 2.1+ requirements must be specified explicitly in the prompt, not assumed.
