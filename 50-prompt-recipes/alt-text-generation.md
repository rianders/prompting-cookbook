# Prompt Recipe: Alt-Text Generation

## Goal
Generate a draft alt-text description for an uploaded image or figure.

## Use this when
- you need a first draft of alt text for a course image, chart, figure, or slide
- you want the description to reflect the teaching purpose of the image, not just visible objects

## Gather these materials
- the image or figure
- surrounding slide, page, or assignment context
- course vocabulary or discipline-specific terms
- audience or student level
- any platform or accessibility guidance you need to follow

## Copy/paste prompt
```text
You are helping me draft alt text for course materials.

Use the attached materials as the primary source of truth:
- the image or figure
- the surrounding page, slide, caption, or assignment context
- any course vocabulary or instructor notes I provide
- any accessibility or platform-specific constraints I provide

Task:
Write draft alt text that helps a student understand the instructional purpose of this image.

Important constraints:
- Base the description on what is actually visible and on the supplied course context.
- Do not invent details that are not visible or not supported by the accompanying materials.
- Prioritize the educationally relevant content of the image over decorative detail.
- If the image appears to be complex and may need a longer description, note that clearly.
- If any important label, axis, or small text is unreadable, mark it as [UNCERTAIN].

Return:
1. concise alt text draft
2. if needed, a short longer-description draft
3. a note explaining which course context shaped the description
4. any [UNCERTAIN] details that need human review
```

## Watchouts
- Do not treat generic image-captioning output as sufficient for teaching materials.
- Do not omit chart labels, equations, or spatial relationships that matter for learning.
- Do not include interpretations that go beyond what the image and context support.
- Do not assume decorative images need long descriptions if they are not instructionally relevant.

## Revision moves
- add the surrounding paragraph, slide title, or assignment directions if the result is too generic
- add discipline-specific vocabulary if the description uses vague everyday language
- ask for a shorter version if the alt text is too long for the platform
- ask for a longer description if the figure is complex and the short alt text cannot carry the meaning

## See also
- [Accessibility](../10-use-cases/accessibility.md)
- [Best Practices and UDL](../20-constraints/best-practices-udl.md)
- [Alt-Text Generation Example](../60-examples/alt-text-generation-example.md)
