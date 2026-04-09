# Accessibility

## Use case
Use AI to transform inaccessible or difficult-to-use teaching materials into more structured, accessible learning components.

## Common tasks
- draft alt text for course images, figures, and charts
- convert dense handouts into more structured, readable learning materials
- identify inaccessible assumptions in an activity or assignment
- turn static course materials into formats that work better in Canvas or with assistive technology

## What to gather first
- the original file or image
- surrounding course context
- accessibility requirements or accommodation priorities
- any platform constraints such as Canvas, PDF, or HTML delivery

## Best prompt pattern
- tell the model what the material is for in the course
- provide the source file as the primary source of truth
- tell the model not to invent unreadable or missing details
- require it to flag uncertainty when labels, text, or visuals are unclear

## Watchouts
- generic image captioning is not the same as instructionally useful alt text
- accessibility improvements should not remove course-specific meaning
- scanned or image-based materials may still need human cleanup after AI assistance

## Start here
- [Alt-Text Generation](../50-prompt-recipes/alt-text-generation.md)
- [Alt-Text Generation Example](../60-examples/alt-text-generation-example.md)
- [Best Practices and UDL](../20-constraints/best-practices-udl.md)
