# Policy-Aware Prompting

## Purpose
Prompts should reflect privacy, data handling, and approved-tool constraints.

## Use this when
- the task involves student work, grades, records, or institution-specific materials
- you need to stay within approved-tool guidance
- you want the model to propose a safer workflow when the requested task is not allowed as stated

## Key rules to embed in prompts
- identify the approved tool or environment
- state what data cannot be shared
- tell the model not to invent institutional rules
- require the model to flag human-review or handoff points

## Typical prompt constraints
- do not include student names, IDs, or identifying details
- use only the supplied policy guidance as the source of truth
- if the task crosses a policy boundary, stop and propose a safer alternative
- prefer redacted or synthetic examples when possible

## Watchouts
- a useful output may still come from an unsafe workflow
- redaction can fail if contextual details still identify a student
- policy-safe prompting is not a substitute for actual policy review

## Start here
- [Policy-Safe Generation](../50-prompt-recipes/policy-safe-generation.md)
- [Policy-Safe Generation Example](../60-examples/policy-safe-generation-example.md)
