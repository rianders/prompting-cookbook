# Prompt Recipe: Hosted Activity Generation

## Goal
Generate an interactive activity with awareness of deployment and hosting constraints.

## Use this when
- you want a low-stakes interactive activity

## Gather these materials
- module objective
- vocabulary or concepts to practice
- student level
- accessibility requirements
- hosting or Canvas constraints

## Copy/paste prompt
```text
You are both an instructional designer and a front-end learning activity developer.

Use the attached module materials as the primary source of truth:
- module overview
- learning objectives
- reading or vocabulary list
- instructor notes
- course values and design constraints

Task:
Create a small interactive learning activity that helps students practice and confirm understanding before moving on.

Technical requirements:
- output a single self-contained HTML file
- include HTML, CSS, and JavaScript in one file
- do not use external dependencies
- include a completion or summary section students can use as a submission artifact if needed

Accessibility requirements (WCAG 2.1+):
- use semantic HTML elements (headings, lists, buttons, labels) rather than styled divs
- all interactive elements must be reachable and operable by keyboard alone (Tab, Enter, Space)
- associate all form inputs and interactive controls with visible labels using <label> or aria-label
- do not use color as the only means of indicating correct answers, errors, or required fields
- text and background color combinations must meet a contrast ratio of at least 4.5:1
- do not autoplay audio or video
- if the activity includes images or diagrams, include appropriate alt text

Return:
1. a short description of the activity
2. the complete self-contained HTML file
3. a note describing how it supports the module learning objective
4. a short WCAG 2.1+ checklist confirming which accessibility requirements are met in the output
```

## Watchouts
- AI-generated HTML should always be opened in a browser and tested with keyboard-only navigation before sharing with students.
- Color contrast must be verified with a contrast checker tool — the model cannot measure contrast ratios reliably. Use the [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/).
- The completion section is a summary artifact only; it is not a secure submission. Use your LMS for graded submissions.

## Revision moves
- If the output fails keyboard navigation, ask the model to replace click-only event handlers with keyboard-accessible alternatives.
- If contrast is insufficient, ask the model to adjust the color values and specify the target contrast ratio (4.5:1 minimum).
- If the activity is too long for one sitting, ask for a version split into two or three shorter sections.

## See also
- [Best Practices: UDL and WCAG 2.1+](../20-constraints/best-practices-udl.md)
- [Infrastructure Reality](../30-environment/infrastructure-reality.md)
- [Hosted Activity Generation Example](../60-examples/hosted-activity-generation-example.md)
