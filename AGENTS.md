# Sharing Workspace Instructions

## Scope and paths

- Treat the sharing directory as the base for paths supplied in prompts. After changing directories, resolve paths against that base explicitly. Use relative paths in inputs, documentation links and shared commands; generated artifacts may contain verified local absolute paths.
- Store case projects, documents, temporary test data and evidence under the appropriate output/ project. Keep reference/ read-only. Overwrite same-name generated outputs; do not create versioned copies.
- Install global skill definitions and supporting files under the current user's home directory in .agents/skills/. Keep skills generic; callers supply URLs, documents and destinations. Application scripts and evidence belong to the case projects.
- Use English in AGENTS.md instructions. Produce Chinese product UI and case documentation. Do not save raw conversation transcripts or user quotations; save structured task prompts and confirmed requirements instead.

## Environment

- Before Python or browser automation, run prepare-environment.sh or prepare-environment.bat according to README.md. Resolve failures and rerun before claiming readiness; do not delete environments to hide failures.
- Activate the named conda environment for every new terminal: Bash/Zsh uses source .environment/activate.sh; Windows CMD uses call .environment\activate.bat. PowerShell can enter an activated CMD with cmd /k .environment\activate.bat.
- If terminal state cannot persist, read .environment/environment.json and use conda run -n with the recorded name. Set PLAYWRIGHT_BROWSERS_PATH to the environment's playwright-browsers directory.
- Install all Python dependencies into this shared environment using python -m pip. Do not create another venv or borrow global/unrelated project dependencies. This overrides skill defaults for Python isolation.
- Setup scripts install and register Chrome DevTools MCP. Installation/configuration, browser attachment and successful capture are separate states. For reference capture, follow the global website-feature-capture skill and reuse the user's existing target tab.

## Working and verification

- Before work, read applicable AGENTS.md files, the corresponding case explanation and prompt, the knowledge index and relevant completed artifacts.
- Verify and lock dependency versions during implementation. Commands and scripts must support Windows, macOS and Linux, including paths with spaces and non-ASCII characters. Report platforms actually tested.
- Distinguish planned, created, running and verified states. Preserve real failure evidence; never report unexecuted checks as passed. Do not operate production data or unrelated projects.
- After successfully starting a reviewable local site, include its actual clickable URL in the reply, whether the service remains running and how to stop it. A URL stored only in a file is insufficient.
- Keep stage inputs, design decisions, deployment records and evidence indexed. Update affected projects when requirements or contracts change. Do not commit Git unless requested.
