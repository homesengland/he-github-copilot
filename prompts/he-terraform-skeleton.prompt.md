# Infrastructure as Code Migration Task

You are an expert Terraform developer specializing in Azure infrastructure provisioning and Azure DevOps pipelines.

## Objective
Clone the baseline infrastructure repository into the temp folder and create a new, fully customized codebase for a new project with updated configurations, documentation, and CI/CD pipelines in the current folder path on the terminal.

## Task Requirements

### 1. Repository Setup
- Clone the source repository: `https://dev.azure.com/homesengland/IRS/_git/he-irs-infrastructure`
- Create a new directory structure for the target project
- Initialize appropriate version control settings

### 2. Project Configuration
**Project Details:**
- **Full Name**: Example
- **Short Name**: exa
- **Naming Convention**: Use `exa` as the resource prefix throughout all infrastructure code

### 3. Code Migration & Customization
Update the following components with the new project identifiers:

#### Terraform Code
- [ ] Replace all resource name prefixes with `exa`
- [ ] Update all variable definitions in `variables.tf` files
- [ ] Modify `terraform.tfvars` or `.tfvars` files with new project values
- [ ] Update resource group names, storage account names, and other Azure resource identifiers
- [ ] Ensure all module references are correct
- [ ] Update backend configuration (if applicable)
- [ ] Validate terraform formatting (`terraform fmt`)

#### Azure Pipelines
- [ ] Update pipeline YAML files with new project name and short name
- [ ] Modify variable groups and pipeline variables
- [ ] Update service connection references
- [ ] Adjust artifact names and paths
- [ ] Update environment-specific configurations (dev, test, prod)

#### Documentation
- [ ] Update README.md with new project name and description
- [ ] Modify setup instructions with project-specific details
- [ ] Update architecture diagrams or references (if present)
- [ ] Revise prerequisites and deployment instructions
- [ ] Update contribution guidelines with new repository information

#### GitHub Copilot Instructions
- [ ] Update `.github/copilot-instructions.md` or similar files
- [ ] Modify any project-specific AI assistance rules
- [ ] Ensure coding standards reflect the new project context

#### .results Folder
- [ ] Copy relevant result files and update paths/names
- [ ] Ensure any output files reflect the new project configuration

### 4. Validation Steps
- [ ] Run `terraform init` to verify configuration
- [ ] Run `terraform validate` to check syntax
- [ ] Run `terraform plan` to preview infrastructure changes
- [ ] Review all file changes for accuracy
- [ ] Ensure no references to the old project name remain
- [ ] Check for hardcoded values that need updating

### 5. Final Deliverables
Provide a complete, ready-to-deploy codebase with:
- ✅ All Terraform modules properly configured
- ✅ Azure Pipeline YAML files ready for execution
- ✅ Comprehensive README with deployment instructions
- ✅ Updated GitHub Copilot instruction files
- ✅ Clean git history (if initializing new repo)
- ✅ Ensure .terraform is added to the .gitignore file

## Important Notes
- **DO NOT STOP** until ALL checklist items are completed
- Maintain consistent naming conventions throughout
- Preserve the infrastructure architecture from the source repository
- Ensure all secrets and sensitive values use proper variable references
- Follow Azure and Terraform best practices
- Test configuration validity before marking complete

## Expected Behavior
Work through each section systematically, using the manage_todo_list tool to track progress. Mark items as in-progress when starting and completed immediately after finishing. Continue until all tasks are verified complete.