# Prompt Recipe: UDL-Aware Activity Design

**UDL** stands for Universal Design for Learning — a framework for designing instruction that works for the widest range of learners from the start, rather than as an accommodation after the fact. It focuses on three principles: multiple means of engagement, multiple means of representation, and multiple means of action and expression.

This recipe pairs UDL review with **WCAG 2.1+** accessibility checks. UDL governs how instruction is designed; WCAG 2.1+ governs whether the materials and interfaces are technically accessible.

## Goal
Review or redesign an activity using Universal Design for Learning (UDL) principles and WCAG 2.1+ accessibility criteria.

## Use this when
- you want to review an existing activity for inclusiveness before using it
- you are designing a new activity and want UDL and accessibility built in from the start
- you are converting a face-to-face activity to a digital or hybrid format

## Gather these materials
- activity or assignment description
- learning objective
- student level and any known accommodation contexts
- course values
- delivery format (Canvas page, HTML activity, in-person, hybrid)

## Copy/paste prompt
```text
You are an instructional design assistant reviewing my activity design for Universal Design for Learning (UDL) alignment and WCAG 2.1+ accessibility.

Use the attached materials as the primary source of truth:
- activity description
- learning objective
- course notes or values
- student level and any accommodation context I provide
- delivery format and platform constraints I provide

Task:
Review this activity against UDL principles and WCAG 2.1+ accessibility criteria.

UDL focus areas:
1. multiple means of engagement — does the activity offer more than one way to participate?
2. multiple means of representation — is content available in more than one format or modality?
3. multiple means of action and expression — can students show understanding in more than one way?
4. plain language and clarity — are instructions unambiguous and free of unexplained jargon?
5. assumptions about prior knowledge, tools, or access — what does the activity assume students have?

WCAG 2.1+ focus areas:
6. non-text content — do all images, diagrams, and figures have appropriate alt text? (SC 1.1.1)
7. color and contrast — is color the only means of conveying any information? (SC 1.4.1, 1.4.3)
8. keyboard access — can all interactive elements be reached and used without a mouse? (SC 2.1.1)
9. clear labels and headings — are interactive elements and sections clearly labeled? (SC 2.4.6)
10. reading level and language — is the reading level appropriate for the student audience? (SC 3.1.5)

Important constraints:
- Base the review on the supplied activity and course materials.
- Do not flag issues that do not apply to the delivery format I described.
- If a WCAG check cannot be completed without seeing the actual digital artifact, note it as [NEEDS HUMAN REVIEW].
- If a recommendation conflicts with a specific course constraint I provided, flag it instead of overriding it.

Return:
1. strengths — what the activity already does well for UDL and accessibility
2. gaps — specific UDL or WCAG 2.1+ issues found
3. suggestions — concrete changes for each gap
4. a short revised version of the activity or activity instructions if appropriate
5. any [NEEDS HUMAN REVIEW] items requiring a person to check the actual artifact
```

## Watchouts
- Do not treat UDL as a checklist decoration added after the activity is finished.
- Do not assume that adding more options automatically improves UDL — options must serve the learning goal.
- Do not accept AI-generated WCAG verdicts on HTML or interactive artifacts without testing in an actual browser or with a screen reader.
- Color contrast must be verified with a contrast checker tool, not estimated from a description.

## Revision moves
- If the review is too generic, add the specific platform (Canvas, standalone HTML, in-person) and student accommodation context.
- If the WCAG checks are incomplete, share the actual HTML or image artifact for a more targeted review.
- If the activity cannot be revised to meet all UDL principles, ask for a phased improvement plan.

## See also
- [Best Practices: UDL and WCAG 2.1+](../20-constraints/best-practices-udl.md)
- [Accessibility](../10-use-cases/accessibility.md)
- [Alt-Text Generation](../50-prompt-recipes/alt-text-generation.md)
- [UDL-Aware Activity Design Example](../60-examples/udl-aware-activity-design-example.md)
