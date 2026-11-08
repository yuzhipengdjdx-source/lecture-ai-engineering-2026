# Repository Guidance

## Project

- This is the AIE2026 Japanese-language exercises repository. Keep learner-facing explanations and documentation in Japanese, matching the surrounding files.
- The project grows a learning-support agent across lectures. Check the relevant `lectures/NN/problem.md`, nearby implementation, and tests before changing lecture-specific behavior.
- `app/` contains the agent, tools, API configuration, judge, and MCP integration. `data/` contains the glossary, lecture summaries, and evaluation data. `tests/` contains automated tests. Student answers belong in `lectures/NN/answer.md` and should only be edited when requested.

## Environment and Dependencies

- Target Python 3.12. Use `uv` for environment and dependency management.
- Dependencies are intentionally pinned for the course. Do not upgrade or re-resolve them unless the task requires a dependency change. If dependencies do change, update `pyproject.toml` and `uv.lock` consistently.
- Read API keys only through the existing configuration. Never add secrets to source files, tests, notebooks, documentation, or commits.
- Keep automated tests independent of paid APIs; use the existing test model or mocks for LLM-facing behavior.

## Validation

- Install/synchronize the locked environment with `uv sync --frozen` when needed.
- Run the full test suite with `uv run pytest -q`.
- Tests are configured in `pyproject.toml` to run from `tests/` with the repository root on the Python path.

## Change Conventions

- Keep changes focused and follow existing Python and pytest patterns.
- Preserve the public CLI and documented commands unless the task explicitly changes them.
- Update relevant lecture instructions or README documentation when user-facing behavior or setup changes.