# Prompt Recipe: Grounded Grading and Feedback

## Goal
Use a rubric, learning objectives, module materials, and course framing to support grading or feedback.

## Use this when
- you want rubric-grounded feedback
- you want to avoid zero-shot grading

## Gather these materials
- student response
- rubric
- assignment description
- learning objectives
- module materials
- course values
- assigned readings

## Copy/paste prompt
```text
You are helping me evaluate student work using my course materials, not general background knowledge.

Use the attached materials as the primary source of truth:
- student response
- rubric
- assignment description
- learning objectives
- module materials
- any course values or time-frame notes I provide

Task:
Evaluate this response using the rubric and the course-specific framing of the assignment.

Important constraints:
- Base your evaluation on the rubric, learning objectives, and supplied course materials.
- Do not grade based on general outside expectations unless they are required by the rubric.
- If a judgment depends on missing information, mark it as [UNCERTAIN].

Return:
1. score or evaluation by rubric category
2. short feedback note
3. one specific next step for revision or improvement
4. one sentence explaining how the response aligns or does not align with the course goals
```
