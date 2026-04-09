# Prompting Cookbook

This revised cookbook is organized around the examples, use cases, constraints, and tooling shown in the April 10, 2026 Rutgers UOES presentation on prompting and context engineering.

## Best Starting Files
- [START-HERE.md](START-HERE.md)
- [CHOOSE-YOUR-TASK.md](CHOOSE-YOUR-TASK.md)
- [FACULTY-WORKFLOW-EXAMPLE.md](FACULTY-WORKFLOW-EXAMPLE.md)
- [COMMON-MISTAKES-AND-WARNINGS.md](COMMON-MISTAKES-AND-WARNINGS.md)

## GitHub Pages / MkDocs
- Site config: `mkdocs.yml`
- Python project: `pyproject.toml`
- Pages workflow: `.github/workflows/pages.yml`
- Published preview: `https://rianders.github.io/prompting-cookbook/`

To preview locally:
```bash
uv sync --group docs
uv run mkdocs serve
```

Local preview URL:
```text
http://127.0.0.1:8000/
```
