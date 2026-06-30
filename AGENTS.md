# AGENTS.md

Always-on instructions for coding agents in this repository.

## 1) Collaboration Defaults

- Prefer small, focused, behavior-safe changes over broad refactors.
- Reuse existing patterns and helpers before creating new abstractions.
- Do not modify unrelated files.
- If requirements are ambiguous, ask a single clear question before implementing.

## 2) Code Quality Bar

- Prioritize correctness and maintainability over speed.
- Keep type safety intact; avoid `any` unless strongly justified.
- Handle errors explicitly; do not swallow failures silently.
- Add brief comments only where logic is non-obvious.

## 3) Change Workflow

1. Discover existing stack and project conventions from current files.
2. Plan the minimal complete implementation.
3. Implement in coherent batches (avoid repeated micro-edits).
4. Run available validation commands.
5. Summarize what changed and how it was verified.

## 4) Validation Rule

- Run only checks that already exist in the repository.
- Prefer this command discovery order:
  1. `package.json` scripts (`npm run <script>`)
  2. `Makefile` targets (`make <target>`)
  3. Python (`pyproject.toml`, `requirements.txt`, `pytest`)
  4. Native build tools (`go.mod`, `Cargo.toml`, `pom.xml`, `build.gradle`)
- If no test/build tooling exists yet, state that clearly in the final report.

## 5) Documentation Rule

Update documentation when behavior, setup, or developer workflow changes.

Minimum docs expected once project is scaffolded:

- `README.md` (setup, run, test)
- `CONTRIBUTING.md` (workflow and quality expectations)
- `ARCHITECTURE.md` (boundaries and major components)

## 6) Repository Conventions (Fill In)

Update this section when conventions are introduced:

- **Primary stack:** `<node/python/go/...>`
- **Install command:** `<npm ci / pip install -r requirements.txt / ...>`
- **Build command:** `<npm run build / ...>`
- **Test command:** `<npm test / pytest / go test ./... / ...>`
- **Lint/format command:** `<npm run lint / ruff check / ...>`
- **Key directories:** `<src/, tests/, apps/, packages/, ...>`
- **Environment notes:** `<OS quirks, required services, secrets handling>`
