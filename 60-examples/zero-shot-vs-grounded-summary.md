# Example: Zero-Shot vs Grounded Summary

## Scenario
An instructor wants a short summary for students about a local New Brunswick community topic that appears in the course materials.

## Source files
- `sources/xrcourse/Latino Migration to New Brunswick Today (1).docx`

## Zero-shot request
```text
Summarize this topic.
```

## Why zero-shot is weak
- It does not identify which text should be summarized.
- It encourages the model to rely on general background knowledge.
- It gives no audience, scope, or fidelity constraint.

## Grounded request
```text
You are helping me summarize a course reading for students.

Use the attached reading as the primary source of truth.

Task:
Write a short summary of this reading for students in my course.

Important constraints:
- Summarize only what is supported by the supplied document.
- Do not add outside historical or political context unless it appears in the reading.
- Keep the summary concise and readable for students encountering this material for the first time.
- If a detail is unclear in the source, mark it as [UNCERTAIN].

Return:
1. a 1-paragraph summary
2. 3 key takeaways
3. one sentence explaining why this reading matters for the course
```

## Materials provided
- the assigned reading itself
- optionally, the course framing for why students are reading it

## Expected output shape
- a summary constrained to the supplied document
- key takeaways suitable for course use
- no hallucinated background additions

## Review notes
- Check whether the summary introduces facts not present in the reading.
- Check whether the reading's relevance is tied back to the course.
- Check whether uncertainty is surfaced rather than smoothed over.

## Why this example is useful
This example shows that summarization is not automatically grounded just because the task sounds simple. The source document still has to be named and prioritized.
