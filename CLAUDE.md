# CLAUDE.md

This file provides guidance for AI assistants (Claude Code and similar tools) working in this repository.

## Repository Overview

This is a new, empty repository hosted at `calpicocodes/test`. No application code, framework, or build system has been established yet. When the first code is added, update this file to reflect the actual stack, structure, and conventions.

## Git Workflow

**Active development branch:** `claude/add-claude-documentation-dZCLH`

### Branch conventions
- Feature branches: `feature/<short-description>`
- Bug fixes: `fix/<short-description>`
- Claude-initiated branches: `claude/<task-description-with-id>`

### Commit conventions
- Write commit messages in the imperative mood: "Add feature" not "Added feature"
- Keep the subject line under 72 characters
- Reference the task or issue in the body when relevant
- Never skip pre-commit hooks (`--no-verify`)

### Push and PR workflow
1. Push to the designated feature branch: `git push -u origin <branch-name>`
2. Always open a draft PR after pushing a new branch
3. Never force-push to `main`/`master` without explicit user permission

## Development Conventions

### Code style
- Prefer editing existing files over creating new ones
- Do not add comments that explain *what* code does — only add them when the *why* is non-obvious
- No multi-line docstrings or comment blocks unless the project style requires them
- Match the indentation, naming, and style of surrounding code

### Error handling and validation
- Only validate at system boundaries (user input, external APIs)
- Do not add error handling for scenarios that cannot happen
- Trust framework and internal library guarantees

### Scope discipline
- Do not add features, abstractions, or refactors beyond what the task requires
- Do not design for hypothetical future requirements
- Three similar lines of code is better than a premature abstraction

### Security
- Never introduce command injection, XSS, SQL injection, or other OWASP Top 10 vulnerabilities
- Never commit secrets, credentials, or `.env` files
- Validate all external input at system boundaries

## File and Directory Structure

_To be documented once the project structure is established._

## Build, Test, and Lint Commands

_To be documented once a build system and toolchain are chosen._

## Key Conventions for AI Assistants

- Always read a file before editing it
- Prefer parallel tool calls for independent operations
- Confirm with the user before taking destructive or hard-to-reverse actions (force push, file deletion, dropping data, etc.)
- Do not push to branches other than the designated development branch without explicit permission
- After pushing, always create a draft PR if one does not already exist
- Do not use emojis unless the user explicitly requests them
- Keep responses short and concise; match response length to task complexity
