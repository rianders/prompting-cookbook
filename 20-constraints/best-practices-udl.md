# Best Practices: Universal Design for Learning (UDL) and WCAG 2.1+

## Purpose
Prompt constraints should reflect pedagogical and accessibility best practices, not only content goals.

**Universal Design for Learning (UDL)** is a framework for designing instruction that works for the widest range of learners from the start. It focuses on three principles: multiple means of engagement, multiple means of representation, and multiple means of action and expression.

**WCAG 2.1+** (Web Content Accessibility Guidelines) is the technical accessibility standard targeted for all course materials and digital activities in this cookbook. WCAG 2.1 success criteria are organized under four principles: Perceivable, Operable, Understandable, and Robust (POUR).

UDL and WCAG 2.1+ are complementary. UDL governs how instruction is designed; WCAG 2.1+ governs whether the materials and interfaces that deliver it are technically accessible.

## Use this when
- reviewing an activity for inclusiveness or clarity
- designing a new task that should support multiple ways of participation
- checking whether instructions assume too much prior knowledge or tool familiarity
- evaluating whether a generated HTML activity or digital artifact meets accessibility standards

## Good constraints to embed

### UDL constraints
- provide multiple ways for students to engage
- provide multiple ways for students to demonstrate understanding
- use plain language and explicit instructions
- surface assumptions about access, prior knowledge, time, and tools

### WCAG 2.1+ constraints
- all non-text content must have a text alternative (Success Criterion 1.1.1)
- color must not be the only means of conveying information (SC 1.4.1)
- text must meet a minimum contrast ratio of 4.5:1 for normal text (SC 1.4.3)
- all functionality must be accessible by keyboard alone (SC 2.1.1)
- interactive elements must have clear, descriptive labels (SC 2.4.6)
- HTML must use semantic structure (headings, lists, landmarks) (SC 1.3.1)

## Watchouts
- do not treat UDL as a generic decoration layer added after the activity is designed
- do not assume one delivery format works equally well for all students
- do not optimize only for content coverage and ignore friction, clarity, or access
- do not accept AI-generated HTML without checking it for keyboard navigation and contrast
- do not rely on color alone to indicate correct answers, errors, or required fields

## Start here
- [UDL-Aware Activity Design](../50-prompt-recipes/udl-aware-activity-design.md)
- [Alt-Text Generation](../50-prompt-recipes/alt-text-generation.md)
- [Accessibility](../10-use-cases/accessibility.md)
- [Glossary: UDL and WCAG 2.1+](../99-reference/glossary.md)
