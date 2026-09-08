---
name: repo-explorer
description: Create a repository architecture and onboarding guide by inspecting the codebase, its tooling, and its primary workflows.
---

# Repository Explorer

Use this skill when the user needs to understand an unfamiliar repository or needs an onboarding document grounded in the repository's actual contents.

## Workflow

1. Inspect the repository structure, including source, tests, configuration, documentation, scripts, and CI files.
2. Identify the application or package entry points and trace the main runtime or build paths.
3. Locate the important architectural boundaries: modules, layers, services, data stores, integrations, and shared utilities.
4. Inspect dependency manifests and developer tooling to determine setup, build, test, lint, format, and deployment commands.
5. Read representative files rather than guessing from filenames. Record evidence for each architectural claim.
6. Note conventions, prerequisites, environment variables, generated files, and common failure points.
7. Produce a concise onboarding guide that distinguishes observed facts from reasonable inferences and calls out unknowns.

## Output

Return a Markdown guide with these sections, adapting them to the repository:

- **What this repository does**: one short, evidence-based summary.
- **Quick start**: prerequisites, installation, configuration, and the first useful command.
- **Repository map**: a compact table of important directories and files.
- **Architecture**: the main components and how requests, data, or jobs move between them. Use a Mermaid diagram when it clarifies relationships.
- **Key workflows**: development, testing, build, deployment, and any important background or CLI workflows.
- **Configuration and integrations**: environment variables, external services, databases, queues, APIs, and authentication.
- **Where to make changes**: map common change types to the owning modules and tests.
- **Troubleshooting**: likely setup or runtime problems and how to diagnose them.
- **Open questions**: facts that could not be verified from the repository.

Use repository-relative file links when citing local evidence. Do not invent commands, services, or architecture. If the repository is empty or incomplete, say so explicitly and provide only the guide that the available evidence supports.

## Quality checks

Before returning the guide, verify that:

- Every command appears in a script, configuration file, or documented tool convention.
- Every architectural claim is supported by a file, symbol, or dependency.
- Setup instructions are ordered and runnable by a new contributor.
- Unknown or inferred details are clearly labeled.
