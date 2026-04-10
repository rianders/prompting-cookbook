# Accessibility

## Use case
Use AI to transform inaccessible or difficult-to-use teaching materials into more structured, accessible learning components.

The target accessibility standard for all materials and digital activities in this cookbook is **WCAG 2.1+** (Web Content Accessibility Guidelines version 2.1 or higher). WCAG 2.1 is organized around four principles — Perceivable, Operable, Understandable, and Robust (POUR) — and applies to any digital content students interact with, including Canvas pages, exported HTML activities, PDFs, and images.

## Common tasks
- draft alt text for course images, figures, and charts (WCAG 2.1 SC 1.1.1)
- convert dense handouts into more structured, readable learning materials
- identify inaccessible assumptions in an activity or assignment
- turn static course materials into formats that work better in Canvas or with assistive technology
- check generated HTML activities for keyboard navigability, contrast, and semantic structure

## What to gather first
- the original file or image
- surrounding course context
- specific WCAG 2.1 success criteria relevant to the material type
- any platform constraints such as Canvas, PDF, or HTML delivery

## Best prompt pattern
- tell the model what the material is for in the course
- provide the source file as the primary source of truth
- name WCAG 2.1+ as the accessibility target in your prompt constraints
- tell the model not to invent unreadable or missing details
- require it to flag uncertainty when labels, text, or visuals are unclear

## Watchouts
- generic image captioning is not the same as instructionally useful alt text
- accessibility improvements should not remove course-specific meaning
- scanned or image-based materials may still need human cleanup after AI assistance
- AI-generated HTML should always be reviewed for keyboard navigation, color contrast (4.5:1 minimum), and semantic markup before sharing with students

## Start here
- [Alt-Text Generation](../50-prompt-recipes/alt-text-generation.md)
- [Alt-Text Generation Example](../60-examples/alt-text-generation-example.md)
- [Best Practices: UDL and WCAG 2.1+](../20-constraints/best-practices-udl.md)
- [Glossary: UDL and WCAG 2.1+](../99-reference/glossary.md)
