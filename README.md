# Cursor AI Rules Repository

This repository stores reusable rules for the Cursor AI code editor to enhance its behavior and ensure consistency across different projects and languages.

## Purpose

The rules defined here provide persistent context, preferences, and workflow guidance to the Cursor AI Agent and Cmd-K features. They help standardize coding practices, enforce project-specific conventions, and improve the quality and relevance of AI-generated code suggestions.

## Structure

Rules are organized within the `.cursor/rules` directory following Cursor's project rules convention:

- **.cursor/rules/**: Contains common rules applicable across multiple languages or the entire project scope.
  - `common-guidelines.mdc`: General best practices for code quality, documentation, commit messages, and AI interaction style.
- **.cursor/rules/gdscript/**: Rules specific to GDScript development.
- **.cursor/rules/go/**: Rules specific to Go development.
- **.cursor/rules/ocaml/**: Rules specific to OCaml development.
- **.cursor/rules/typescript/**: Rules specific to TypeScript development.

## How Cursor Uses These Rules

Cursor automatically detects and applies these rules based on their configuration (`alwaysApply`, `globs`, `agentRequested`) and the context of your work (e.g., files being edited, prompts used).

- **Project Rules:** Rules within `.cursor/rules` are version-controlled and scoped to this project.
- **Nested Rules:** Rules in language-specific subdirectories (`.cursor/rules/go`, etc.) are automatically considered when working with files in corresponding parts of a project (if this structure were mirrored in an actual codebase).

## Contributing

Feel free to add new rules or refine existing ones. Ensure new rules follow the `.mdc` format and include appropriate metadata (`description`, `alwaysApply`, `globs`, etc.).

Refer to the [Cursor Rules Documentation](https://docs.cursor.com/context/rules) for more details on creating and managing rules.
