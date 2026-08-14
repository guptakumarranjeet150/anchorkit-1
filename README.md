````markdown
# AnchorKit

**AnchorKit is an open-source toolkit for building anchor-style payment infrastructure, escrow workflows, smart contract modules, diagnostics, and developer tooling.**

AnchorKit is part of the **Axionvera** ecosystem and is designed as a contributor-friendly monorepo for builders working across payments, contracts, applications, packages, scripts, examples, and tests.

The project focuses on clean architecture, maintainable code, useful documentation, and reliable development workflows.

---

## Overview

AnchorKit provides a foundation for building and maintaining reusable infrastructure around:

- Anchor-style payment workflows
- Payment intent handling
- Smart contract modules
- Escrow-related utilities
- Diagnostics and validation
- Developer tooling
- Configuration management
- Example implementations
- Cross-package testing
- Open-source contributor workflows

The goal is to keep the codebase understandable, testable, and easy for contributors to improve.

---

## Repository Structure

The current repository is organised as a monorepo:

```txt
anchorkit/
├── .github/
├── apps/
├── contracts/
├── docs/
├── examples/
├── issues/
├── packages/
├── scripts/
├── tests/
├── .editorconfig
├── .eslintrc.js
├── .gitignore
├── .npmrc
├── .prettierignore
├── .prettierrc
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENCE
├── package.json
├── pnpm-lock.yaml
├── pnpm-workspace.yaml
├── README.md
├── SECURITY.md
├── tsconfig.base.json
└── turbo.json
```

---

## Core Directories

| Directory | Purpose |
|---|---|
| `apps/` | Application-level projects, demos, dashboards, or frontend surfaces |
| `contracts/` | Smart contract or protocol-related code |
| `docs/` | Project documentation, architecture notes, and guides |
| `examples/` | Example implementations and usage references |
| `issues/` | Structured issue batches or issue-related project planning files |
| `packages/` | Shared libraries, reusable modules, and internal packages |
| `scripts/` | Automation scripts and developer tooling |
| `tests/` | Shared tests, integration tests, fixtures, and regression coverage |
| `.github/` | GitHub workflows, issue templates, PR templates, and repository automation |

---

## Project Goals

AnchorKit aims to:

- Provide clean and reusable modules for anchor-related infrastructure
- Support payment, escrow, contract, and diagnostic workflows
- Keep package boundaries clear across the monorepo
- Improve reliability through testing and validation
- Support contributor-friendly development
- Maintain clean formatting, linting, and review standards
- Encourage meaningful open-source contributions

---

## Requirements

Before running the project locally, make sure you have the following installed:

- Git
- Node.js
- pnpm
- Rust
- Cargo

Check your versions:

```bash
node --version
pnpm --version
rustc --version
cargo --version
```

If `pnpm` is not installed, install it with:

```bash
npm install -g pnpm
```

Install Rust and Cargo with `rustup`:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

After installation, confirm Rust and Cargo are available:

```bash
rustc --version
cargo --version
```

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/Axionvera/anchorkit.git
cd anchorkit
```

Install dependencies:

```bash
pnpm install
```

Run a full project build:

```bash
pnpm build
```

Run the test suite:

```bash
pnpm test
```

---

## Development Commands

### Install Dependencies

```bash
pnpm install
```

---

### Build the Monorepo

```bash
pnpm build
```

This uses the project workspace and build configuration to build the relevant apps and packages.

---

### Run Development Mode

If the repository has development scripts configured, run:

```bash
pnpm dev
```

---

### Run Tests

Run all configured tests:

```bash
pnpm test
```

Run tests for a specific package or app if configured:

```bash
pnpm --filter <package-name> test
```

Example:

```bash
pnpm --filter @anchorkit/core test
```

---

### Lint the Codebase

```bash
pnpm lint
```

---

### Format the Codebase

```bash
pnpm format
```

Check formatting without changing files if configured:

```bash
pnpm format:check
```

---

### Type Check

```bash
pnpm typecheck
```

---

## Working With Contracts

The `contracts/` directory contains contract or protocol-related code.

If the contracts use Rust/Cargo, move into the contract directory:

```bash
cd contracts
```

Build the contracts:

```bash
cargo build
```

Run contract tests:

```bash
cargo test
```

Run a faster compile check:

```bash
cargo check
```

Format Rust code:

```bash
cargo fmt
```

Run Clippy:

```bash
cargo clippy
```

Treat Clippy warnings as errors:

```bash
cargo clippy -- -D warnings
```

Return to the repository root:

```bash
cd ..
```

---

## Recommended Local Check

Before opening a pull request, run the relevant checks from the repository root:

```bash
pnpm install
pnpm build
pnpm test
pnpm lint
pnpm typecheck
```

If your change touches Rust contracts, also run:

```bash
cd contracts
cargo fmt
cargo clippy -- -D warnings
cargo test
cargo build
cd ..
```

A clean contribution should pass formatting, linting, tests, type checks, and build checks.

---

## Apps

The `apps/` directory is intended for application-level projects.

These may include:

- Demo applications
- Dashboards
- Frontend interfaces
- Integration examples
- Contributor-facing tools

Apps should use shared packages where possible instead of duplicating logic.

---

## Packages

The `packages/` directory contains reusable modules and shared libraries.

Packages may include:

- Core types
- Payment utilities
- Anchor workflow helpers
- Escrow utilities
- Diagnostics modules
- Validation helpers
- Configuration tools
- Shared UI or developer tooling

Package code should be reusable, tested, and clearly scoped.

---

## Contracts

The `contracts/` directory contains smart contract or protocol-related code.

Contract contributions should prioritise:

- Correctness
- Security
- Clear state handling
- Strong tests
- Safe error handling
- Documentation for public behaviour
- Avoiding unnecessary complexity

If a contract change affects external consumers, update the relevant docs, examples, or package integrations.

---

## Examples

The `examples/` directory contains sample implementations and usage references.

Examples should be:

- Easy to understand
- Safe to run locally
- Free from real secrets
- Aligned with current package APIs
- Useful for contributors and integrators

---

## Docs

The `docs/` directory contains project documentation.

Documentation may include:

- Architecture notes
- Setup guides
- Contributor guides
- Package usage guides
- Contract behaviour notes
- Testing guides
- Troubleshooting guides

Update documentation whenever behaviour, setup, configuration, or public APIs change.

---

## Scripts

The `scripts/` directory contains automation and developer tooling.

Scripts may be used for:

- Workspace maintenance
- Issue generation
- Build helpers
- Test helpers
- Formatting helpers
- Repository automation

Scripts should be documented when they are intended for contributor or maintainer use.

---

## Tests

The `tests/` directory contains shared test coverage, integration tests, fixtures, or regression tests.

Useful test types include:

- Unit tests
- Integration tests
- Regression tests
- Error-path tests
- Configuration tests
- Contract tests
- Cross-package tests

When adding or changing behaviour, include tests that prove the expected result.

---

## Code Quality

AnchorKit values clean, maintainable code.

Contributions should aim for:

- Clear module boundaries
- Minimal duplication
- Predictable error handling
- Meaningful tests
- Simple implementation
- Good naming
- Useful documentation
- No unrelated rewrites

Avoid large unscoped changes that make review difficult.

---

## Error Handling

Error handling should be consistent and developer-friendly.

Contributions should avoid:

- Unclear panic paths
- Raw string errors where typed errors are better
- Leaking sensitive information
- Hiding useful failure context
- Mixing unrelated error types

Good error handling should be:

- Predictable
- Testable
- Safe
- Easy for developers to understand

---

## Contribution Guidelines

Contributions are welcome.

Before working on an issue:

1. Read the issue carefully.
2. Confirm the expected behaviour.
3. Check the acceptance criteria.
4. Keep the scope focused.
5. Avoid unrelated changes.
6. Add tests where relevant.
7. Update documentation where needed.
8. Run the required local checks.

Please also review:

- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- `SECURITY.md`

---

## Pull Request Checklist

Before submitting a pull request, confirm:

- [ ] The PR solves the linked issue.
- [ ] The implementation is clearly scoped.
- [ ] The code is formatted.
- [ ] Linting passes.
- [ ] Tests pass.
- [ ] Type checks pass where applicable.
- [ ] Contract checks pass if contracts were changed.
- [ ] Documentation is updated where needed.
- [ ] No unrelated files were changed.
- [ ] The PR description clearly explains the change.

Recommended final check:

```bash
pnpm build
pnpm test
pnpm lint
pnpm typecheck
```

For contract changes:

```bash
cd contracts
cargo fmt
cargo clippy -- -D warnings
cargo test
cargo build
cd ..
```

---

## Good First Contribution Areas

Good contribution areas may include:

- Improving tests
- Cleaning up module boundaries
- Fixing small bugs
- Improving documentation
- Adding examples
- Improving diagnostics
- Refactoring duplicated logic
- Strengthening error handling
- Improving package structure

Please avoid low-effort changes that do not meaningfully improve the project.

---

## Maintainer Notes

Maintainers should review contributions based on:

- Issue alignment
- Correctness
- Test coverage
- Code quality
- Maintainability
- Documentation updates
- Security and reliability impact
- Long-term usefulness

A pull request should improve the codebase, not just add activity.

---

## Security

If you discover a security issue, please do not open a public issue with sensitive details.

Review `SECURITY.md` for the correct reporting process.

---

## Project Status

AnchorKit is actively evolving.

Some parts of the project may be experimental, incomplete, or subject to refactoring as the architecture becomes more stable.

Contributors should read existing issues and documentation before making major changes.

---

## Licence

This project is licensed under the terms described in the `LICENCE` file.

---

## Part of Axionvera

AnchorKit is part of the Axionvera open-source ecosystem.

Axionvera is focused on building reliable infrastructure for digital finance, developer tooling, automation, and protocol systems.

Explore the organisation:

```txt
https://github.com/Axionvera
```

---

## Build With AnchorKit

Explore the codebase.  
Run the tests.  
Pick a meaningful issue.  
Help improve the project.

**AnchorKit is built for maintainable infrastructure and open contribution.**
````
