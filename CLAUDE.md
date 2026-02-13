# CLAUDE.md — Conventions for Claude Code

## Project
Avantaga — AI-enabled financial analysis and decision services.

## Repo structure
```
prompts/        → .yml, .md prompt packs and persona definitions
notebooks/      → .ipynb notebooks (run in Google Colab)
scripts/        → .py standalone scripts
data/           → .csv, .json reference data (small files only)
docs/           → .md documentation and architecture notes
config/         → .yml, .json configuration files
```

## Rules
- Python 3.10+ only. Keep dependencies minimal.
- All scripts must run in Google Colab without modification (no local-only paths).
- Use relative paths, never absolute Windows paths in code.
- Small .csv and .json in `data/`. Large files stay on Google Drive — never commit files > 5 MB.
- Secrets and credentials must never be committed. Use .env or environment variables.
- Do not touch or modify files in `data/raw/` without explicit instruction.

## Code style
- Clear variable names, no abbreviations.
- Docstrings on all functions.
- Type hints where practical.
- Print/log key outputs so Colab cells show results inline.

## Commit conventions
- Short imperative subject line (e.g., "Add revenue forecast script")
- Reference what changed and why if non-obvious.

## Documentation
- All docs in Markdown (.md).
- Use YAML front matter for metadata where useful.
