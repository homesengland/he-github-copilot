# he-github-copilot

Home to bespoke prompts, instructions, and helper scripts used to standardise and enhance GitHub Copilot usage across Homes England projects.

## Purpose
- Curate reusable Copilot prompts for consistent outputs.
- Store instructional guidance for common tasks and workflows.
- Provide lightweight scripts to automate routine actions.

## Repository Structure
- `instructions/`: Instruction files that give Copilot additional context on how to understand your project and how to build, test and validate its changes.
- `prompts/`: Prompt files for specific workflows (e.g., Terraform skeleton, updating GHCP instructions).
- `scripts/`: Utility scripts to support prompts and workflows.

## Getting Started
- Ensure you have GitHub Copilot enabled in VS Code.
- Browse `prompts/` and open the relevant `.prompt.md` for your task.
- Follow any linked steps in `instructions/` and run supporting scripts from `scripts/` as needed.

## Usage
- Open a prompt file (e.g. `prompts/he-terraform-skeleton.prompt.md`).
- Read the context and copy or adapt the prompt into Copilot Chat.
- Where a prompt references instructions, locate them in `instructions/`.
- If a script is referenced, run it from the repository root.

## Running Scripts
All commands assume macOS with `zsh`:

```zsh
# From repo root
cd /Users/lewisjackson/git/he-github-copilot

# Example: list scripts
ls scripts

# Example: run a helper script (replace with actual filename)
zsh scripts/example.sh
```

## Contributing
- Keep prompts focused, actionable, and scoped to a single workflow.
- Prefer small, composable prompts over monoliths.
- Update `README.md` when adding notable prompts or instructions.
- Use clear filenames: `he-<area>-<purpose>.prompt.md`.

## Relevant Links
- [Adding personal custom instructions for GitHub Copilot](https://docs.github.com/en/copilot/how-tos/configure-custom-instructions/add-personal-instructions)
- [Prompt files](https://docs.github.com/en/copilot/tutorials/customization-library/prompt-files)

## Versioning & Ownership
- Owner: `homesengland`
- Default branch: `main`
- Changes should be reviewed to maintain prompt quality and consistency.

## Disclaimer
Prompts are guidance, not guarantees. Review outputs before use, especially for sensitive or production workflows.
