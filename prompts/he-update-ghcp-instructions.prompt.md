# Prompt: Update Copilot Instructions and .results Markdown

## Goal
Update `.github/copilot-instructions.md` to match the attached instructions and recursively sync all `.results/**/*.md` files to reflect the current branch’s changes.

## Context
- Source of truth: Attached Copilot instructions (provided in session) and `/.github/copilot-instructions.md`.
- Target files/directories:
  - `.github/copilot-instructions.md`
  - `.results/**` (all Markdown files under this folder and subfolders)
- Current date: December 12, 2025

## Tasks
1. Replace `/.github/copilot-instructions.md` content with the provided attachment. Preserve headings, sections, examples, and formatting.
2. Recursively traverse `.results/` and update every `.md` file:
   - Add this synced banner at the top:
     - `Synced with current branch. Last updated: {TODAYS_DATE}. See \`.github/copilot-instructions.md\` for authoritative guidance.`
   - Align terminology and references with `.github/copilot-instructions.md`:
     - Technology stack, pipelines, modules, naming conventions, and integration patterns.
     - Keep file-specific structure; update only where misaligned.
   - Preserve existing working examples; only remove content that clearly conflicts with authoritative instructions.
3. Keep changes minimal, focused, and consistent with repository style.

## Files To Update
- `.github/copilot-instructions.md`
- `.results/README.md`
- `.results/1-techstack.md`
- `.results/4-domains/*.md`
  - `azure_kubernetes_service.md`
  - `azure_networking.md`
  - `kubernetes_cluster_configuration.md`
  - `project_onboarding.md`
  - `cicd_pipeline_orchestration.md`
- `.results/5-style-guides/*.md`
  - `terraform_style_guide.md`
  - `helm_values_style_guide.md`
  - `pipeline_style_guide.md`
  - `bash_script_style_guide.md`
  - `naming_conventions.md`

## Acceptance Criteria
- `.github/copilot-instructions.md` matches the session attachment (content and structure) and reflects this branch.
- Every `.md` file in `.results/**` starts with the synced banner and has content aligned to the updated instructions.
- Headings, code fences, and formatting preserved; no unrelated sections modified.
- Patches applied surgically; no wholesale reformatting.

## Optional Validation
- Verify banners across `.results`:
  ```zsh
  grep -R "Synced with current branch" .results -n
  ```
- Spot-check alignment against Copilot instructions (terminology and module paths).

## Return
- Provide a concise summary of changes and files updated.
- Note any conflicts found and how they were resolved (or flag for review).
