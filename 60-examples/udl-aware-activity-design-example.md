# Example: UDL-Aware Activity Design

## Scenario
An Italian language instructor has an existing advanced lesson and wants to review it against Universal Design for Learning (UDL) principles and WCAG 2.1+ accessibility criteria before using it this semester. The lesson was designed for in-person use and is now being adapted for a hybrid Canvas module.

## Source files
- `sources/italian/advanced_lesson.pdf`

## Weak starting prompt
```text
Make this lesson more accessible.
```

## Why the weak prompt falls short
- "More accessible" is undefined — the model does not know whether the concern is physical access, language level, format, or technical WCAG compliance.
- It does not name a standard (UDL, WCAG 2.1+) so the output could be generic and unverifiable.
- It does not describe the delivery context (Canvas, hybrid, in-person), which determines which checks are relevant.

## Better grounded prompt
```text
You are an instructional design assistant reviewing my activity design for Universal Design for Learning (UDL) alignment and WCAG 2.1+ accessibility.

Use the attached materials as the primary source of truth:
- the advanced Italian lesson PDF
- the delivery context I describe below

Delivery context:
- Course level: advanced Italian language
- Format: hybrid — lesson materials are posted to Canvas; some class time is in-person
- Students may use screen readers, translation tools, or mobile devices to access Canvas content

Task:
Review this lesson against UDL principles and WCAG 2.1+ accessibility criteria.

UDL focus areas:
1. multiple means of engagement — does the lesson offer more than one way to participate or stay motivated?
2. multiple means of representation — is content available in more than one format or modality?
3. multiple means of action and expression — can students demonstrate understanding in more than one way?
4. plain language and clarity — are instructions unambiguous and free of unexplained jargon?
5. assumptions about prior knowledge, tools, or access — what does the lesson assume students have?

WCAG 2.1+ focus areas:
6. non-text content — do all images, diagrams, or figures have appropriate alt text? (SC 1.1.1)
7. color and contrast — is color the only means of conveying any information? (SC 1.4.1, 1.4.3)
8. keyboard access — if any part of this lesson becomes an interactive digital artifact, can it be used by keyboard alone? (SC 2.1.1)
9. clear labels and headings — are sections and interactive elements clearly labeled? (SC 2.4.6)
10. reading level and language — is instruction language appropriate for the student audience? (SC 3.1.5)

Important constraints:
- Base the review on the supplied lesson PDF and the delivery context I described.
- Do not flag WCAG issues that do not apply to a PDF or Canvas page format (e.g., keyboard navigation of a static document).
- If a WCAG check requires inspecting an actual digital artifact not yet created, note it as [NEEDS HUMAN REVIEW].
- Focus suggestions on changes that preserve the lesson's language-learning purpose.

Return:
1. strengths — what the lesson already does well for UDL and accessibility
2. gaps — specific UDL or WCAG 2.1+ issues found in the lesson as supplied
3. suggestions — one concrete change per gap
4. a short revised version of the activity instructions if appropriate
5. any [NEEDS HUMAN REVIEW] items for after the lesson is converted to a digital format
```

## Materials provided
- the advanced Italian lesson PDF as the primary artifact
- delivery context: hybrid Canvas module, advanced language students, possible screen reader or mobile use

## Expected output shape
- a structured review that separates UDL findings from WCAG findings
- concrete, actionable suggestions (not "add more variety" — specific changes to the lesson)
- a [NEEDS HUMAN REVIEW] list for items that depend on the final digital format

## Review notes
- Check whether the UDL suggestions preserve the language-learning purpose and do not water down the advanced level.
- Check whether WCAG flags are relevant to the actual delivery format — some SC are only triggered by interactive or dynamic content.
- If images or diagrams in the PDF lack alt text, verify that the suggestion accounts for how Canvas handles PDF image descriptions.
- Color contrast issues in PDFs may require exporting to HTML or recreating the document in an accessible format.

## Why this example is useful
This example is the first in the cookbook to use the Italian course source materials, showing that the UDL and WCAG review recipe applies across disciplines — not just to XR or technology-focused courses. It also demonstrates that UDL review and WCAG review are distinct but complementary checks, and that some WCAG items cannot be fully evaluated until the final digital artifact exists.
