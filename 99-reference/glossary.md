# Glossary

## Context Engineering
Designing the surrounding materials, constraints, values, and workflow that shape AI behavior. A prompt is one component of context engineering; the full environment includes the source documents, role framing, output constraints, and validation steps you supply alongside it.

## Universal Design for Learning (UDL)
A framework for designing instruction that works for the widest range of learners from the start, rather than retrofitting accommodations after the fact. UDL is organized around three principles:

1. **Multiple means of engagement** — why students learn; motivation, relevance, and choice
2. **Multiple means of representation** — how content is presented; format, modality, and language
3. **Multiple means of action and expression** — how students demonstrate understanding; not just written essays

UDL is not a checklist applied after an activity is designed. It is a lens applied during design. In this cookbook, UDL constraints are embedded into prompt recipes to guide AI output toward more inclusive instructional materials.

**See also:** [CAST UDL Guidelines](https://udlguidelines.cast.org/), [Best Practices: UDL and WCAG 2.1+](../20-constraints/best-practices-udl.md), [UDL-Aware Activity Design](../50-prompt-recipes/udl-aware-activity-design.md)

## WCAG 2.1+ (Web Content Accessibility Guidelines)
The technical accessibility standard targeted for all course materials and digital activities in this cookbook. WCAG 2.1 is published by the W3C and is organized around four principles, known as **POUR**:

1. **Perceivable** — information must be presentable in ways users can perceive (e.g., alt text for images, captions for video)
2. **Operable** — interface components must be navigable by all users (e.g., keyboard access, sufficient time)
3. **Understandable** — content and operation must be understandable (e.g., plain language, clear labels)
4. **Robust** — content must be interpreted reliably by assistive technologies (e.g., valid, semantic HTML)

Key success criteria referenced in this cookbook:

| SC | Name | What it requires |
|---|---|---|
| 1.1.1 | Non-text Content | All images need a text alternative (alt text or longer description) |
| 1.4.1 | Use of Color | Color must not be the only visual means of conveying information |
| 1.4.3 | Contrast (Minimum) | Text must have a contrast ratio of at least 4.5:1 against its background |
| 2.1.1 | Keyboard | All functionality must be operable by keyboard alone |
| 2.4.6 | Headings and Labels | Headings and labels must be descriptive |
| 3.1.5 | Reading Level | Where possible, content should be supplemented for lower reading levels |

"WCAG 2.1+" in this cookbook means WCAG 2.1 at minimum; WCAG 2.2 criteria are also encouraged where applicable.

**See also:** [WCAG 2.1 specification](https://www.w3.org/TR/WCAG21/), [WCAG 2.1 quick reference](https://www.w3.org/WAI/WCAG21/quickref/), [Best Practices: UDL and WCAG 2.1+](../20-constraints/best-practices-udl.md), [Accessibility](../10-use-cases/accessibility.md)

## Grounded Prompt
A prompt that includes the relevant source materials, course context, and explicit constraints rather than relying on the model's background knowledge. Contrast with a zero-shot prompt.

## Zero-Shot Prompt
A prompt that provides no source materials or course context, relying entirely on what the model already knows. Useful for quick exploration but unreliable for course-specific or policy-sensitive tasks.

## [NEEDS REVIEW]
A marker used in prompt recipes and examples to flag output items that require human verification before use — typically because the model was working with incomplete materials or uncertain context.

## [UNCERTAIN]
A marker used specifically in alt-text and image-description prompts to flag visual details that the model could not read clearly from the supplied image.
