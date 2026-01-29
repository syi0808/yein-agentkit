# CONTRIBUTING.md Structure Guide

Generate a CONTRIBUTING.md with the sections below, in this exact order. Adapt the content of each section to match the project's actual tooling, conventions, and structure discovered during codebase analysis.

Every command and configuration reference must be real. Do not include generic placeholder instructions.

---

<sections>

## Section 1: Welcome

A concise welcome message. State the project name and the purpose of this document.

<example>
# Contributing to Screenize

Thank you for your interest in contributing to Screenize. This guide explains how to report issues, suggest improvements, and submit code changes.
</example>

## Section 2: Code of Conduct

If a `CODE_OF_CONDUCT.md` file exists in the repo, link to it. If not, include this inline statement:

<example_no_file>
## Code of Conduct

Please be respectful and constructive in all interactions. We are committed to providing a welcoming and inclusive experience for everyone.
</example_no_file>

<example_with_file>
## Code of Conduct

This project follows our [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before participating.
</example_with_file>

## Section 3: How to Contribute

Three subsections: Reporting Bugs, Suggesting Enhancements, Pull Requests.

<example>
## How to Contribute

### Reporting Bugs

1. Search [existing issues](../../issues) to check if the bug has already been reported
2. If not, open a new issue with:
   - Steps to reproduce the bug
   - Expected behavior vs. actual behavior
   - Your environment (macOS version, Xcode version)
   - Screenshots or screen recordings if applicable

### Suggesting Enhancements

1. Search [existing issues](../../issues) for similar suggestions
2. Open a new issue describing:
   - The problem or use case
   - Your proposed solution
   - Alternatives you considered

### Pull Requests

1. Fork the repository
2. Create a feature branch from `main` (`git checkout -b feature/your-feature`)
3. Make your changes
4. Ensure the project builds without errors
5. Write clear commit messages (see Style Guide below)
6. Push to your fork and open a pull request
7. Fill in the PR description explaining what changed and why
</example>

## Section 4: Development Setup

This section must be derived from the actual project. Describe the exact steps to set up a local development environment.

Check for: build system, dependency manager, IDE requirements, environment variables, required system permissions.

<example_xcode>
## Development Setup

```bash
git clone https://github.com/YOUR_USERNAME/screenize.git
cd screenize
open Screenize.xcodeproj
```

Build with Cmd+B in Xcode. Run with Cmd+R.

**Permissions:** Screenize requires Screen Recording and Accessibility permissions. If permissions break during development, reset them:

```bash
tccutil reset ScreenCapture com.screenize.Screenize
tccutil reset Microphone com.screenize.Screenize
```
</example_xcode>

<example_node>
## Development Setup

```bash
git clone https://github.com/YOUR_USERNAME/project.git
cd project
npm install
npm run dev
```
</example_node>

Pick the example pattern that matches the project type. Use the actual commands, not these examples verbatim.

## Section 5: Style Guide

Derive this from what actually exists in the project. Check for:

1. Linter/formatter config files (`.eslintrc`, `.prettierrc`, `rustfmt.toml`, `.swiftlint.yml`, `.editorconfig`)
2. Code style patterns visible in the source code
3. Commit message conventions from `git log`

<example_with_linter>
## Style Guide

### Code Style

This project uses ESLint and Prettier for code formatting. Run the linter before submitting:

```bash
npm run lint
```

Configuration is defined in `.eslintrc.js` and `.prettierrc`.

### Commit Messages

- Use the imperative mood: "Add feature" not "Added feature"
- Keep the first line under 72 characters
- Reference issue numbers when applicable: `Fix #123`
</example_with_linter>

<example_without_linter>
## Style Guide

### Code Style

Follow the existing patterns in the codebase. Key conventions:
- [List 2-4 actual conventions observed in the code]

### Commit Messages

- Use the imperative mood: "Add feature" not "Added feature"
- Keep the first line under 72 characters
- Reference issue numbers when applicable: `Fix #123`
</example_without_linter>

If the project uses Conventional Commits or another documented standard, describe that specifically.

## Section 6: Testing

Derive from the actual project. Check for test directories, test configuration files, test scripts in build configs, and CI configuration.

<example_with_tests>
## Testing

Run the test suite before submitting a pull request:

```bash
npm test
```

Tests are located in the `__tests__/` directory and use Jest.

To run a specific test file:

```bash
npm test -- --testPathPattern="auth"
```
</example_with_tests>

<example_without_tests>
## Testing

This project does not yet have an automated test suite. When adding new functionality, consider including tests. Contributions that improve test coverage are welcome.
</example_without_tests>

Use the pattern that matches the project's actual state. If tests exist, document the real commands.

</sections>
