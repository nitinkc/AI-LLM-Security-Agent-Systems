# Project guidance

- This repository is a MkDocs Material learning site. Keep existing lesson paths stable when reorganizing navigation unless folder renames are explicitly requested. Curriculum folders use topic-based names: start-here, agent-concepts, architecture-and-workflows, production-operations, and interview-toolkit.
- Set up dependencies with `uv venv` and `uv pip install -r requirements.txt`.
- Preview with `uv run mkdocs serve`.
- Verify with `uv run mkdocs build --strict --site-dir /tmp/ai-llm-security-site` and `git diff --check`.
- Keep navigation.instant disabled for local live reload. Material handles palette preferences; mermaid2 handles diagrams. Avoid reintroducing duplicate theme or Mermaid initializers.
- `_abbreviations.md` is shared through pymdownx.snippets, not a navigation destination.
- The MathJax initializer was removed outside the site refresh and the user explicitly requested leaving that deletion untouched. Existing equation rendering needs browser verification and may require a future initializer fix.
- Editable draw.io diagram sources live in `docs/assets/diagrams/*.drawio` using `adaptiveColors="auto"` and explicit `light-dark(...)` color tokens, exported to `*-light.svg` (`--theme light --embed-svg-fonts false -b 12`) and `*-dark.svg` (`--theme dark --embed-svg-fonts false -b 12`) for MkDocs Material `#only-light` / `#only-dark` switching.
