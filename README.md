<div align="center">

# AnchorKit

### Open-source infrastructure for anchor workflows, payments, contracts, diagnostics, and developer tooling.

AnchorKit is part of the **Axionvera** ecosystem and is designed as a contributor-friendly monorepo for builders working across applications, packages, contracts, scripts, examples, and tests.

<br />

![Open Source](https://img.shields.io/badge/Open%20Source-Yes-0E8A16?style=for-the-badge)
![Monorepo](https://img.shields.io/badge/Monorepo-pnpm%20%2B%20Turbo-3178C6?style=for-the-badge)
![Rust](https://img.shields.io/badge/Rust-Contracts-DEA584?style=for-the-badge)
![TypeScript](https://img.shields.io/badge/TypeScript-Packages-3178C6?style=for-the-badge)
![Built for Builders](https://img.shields.io/badge/Built%20For-Builders-FBCA04?style=for-the-badge)

<br />

**Build reliable infrastructure. Improve the codebase. Contribute meaningfully.**

</div>

---

## Overview

AnchorKit provides a foundation for building and maintaining reusable infrastructure around:

<table>
  <tr>
    <td width="50%">

### Core Infrastructure

- Anchor-style payment workflows
- Payment intent handling
- Smart contract modules
- Escrow-related utilities
- Diagnostics and validation

    </td>
    <td width="50%">

### Developer Experience

- Developer tooling
- Configuration management
- Example implementations
- Cross-package testing
- Open-source contributor workflows

    </td>
  </tr>
</table>

The goal is to keep the codebase understandable, testable, and easy for contributors to improve.

---

## Repository Structure

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
| `.github/` | GitHub workflows, issue templates, PR templates, and repository automation |
| `apps/` | Application-level projects, demos, dashboards, or frontend surfaces |
| `contracts/` | Smart contract or protocol-related code |
| `docs/` | Project documentation, architecture notes, and guides |
| `examples/` | Example implementations and usage references |
| `issues/` | Structured issue batches or issue-related planning files |
| `packages/` | Shared libraries, reusable modules, and internal packages |
| `scripts/` | Automation scripts and developer tooling |
| `tests/` | Shared tests, integration tests, fixtures, and regression coverage |

---

## Project Goals

<table>
  <tr>
    <td width="33%">

### Clean Architecture

Keep modules, packages, contracts, and applications clearly separated.

    </td>
    <td width="33%">

### Reliable Testing

Improve confidence through unit, integration, regression, and contract tests.

    </td>
    <td width="33%">

### Contributor Friendly

Make the project easier to understand, run, review, and improve.

    </td>
  </tr>
</table>

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

Before running the project locally, install:

| Tool | Purpose |
|---|---|
| Git | Clone and manage the repository |
| Node.js | Run JavaScript and TypeScript tooling |
| pnpm | Install and manage workspace dependencies |
| Rust | Build and test Rust modules |
| Cargo | Rust package manager and build tool |

Check your versions:

```bash
node --version
pnpm --version
rustc --version
cargo --version
```

Install pnpm if needed:

```bash
npm install -g pnpm
```

Install Rust and Cargo with `rustup`:

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Confirm Rust and Cargo are available:

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

Build the project:

```bash
pnpm build
```

Run tests:

```bash
pnpm test
```

---

## Development Commands

| Command | Purpose |
|---|---|
| `pnpm install` | Install workspace dependencies |
| `pnpm build` | Build the monorepo |
| `pnpm dev` | Run development mode if configured |
| `pnpm test` | Run configured tests |
| `pnpm lint` | Run lint checks |
| `pnpm format` | Format the codebase |
| `pnpm format:check` | Check formatting without changing files |
| `pnpm typecheck` | Run TypeScript type checks |

---

## Working With Contracts

The `contracts/` directory contains contract or protocol-related code.

Move into the contract directory:

```bash
cd contracts
```

Build contracts:

```bash
cargo build
```

Run tests:

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

Before opening a pull request, run:

```bash
pnpm install
pnpm build
pnpm test
pnpm lint
pnpm typecheck
```

For contract changes, also run:

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

## Main Areas

<table>
  <tr>
    <td width="50%">

### Apps

The `apps/` directory is intended for application-level projects.

Examples may include:

- Demo applications
- Dashboards
- Frontend interfaces
- Integration examples
- Contributor-facing tools

Apps should use shared packages where possible instead of duplicating logic.

    </td>
    <td width="50%">

### Packages

The `packages/` directory contains reusable modules and shared libraries.

Packages may include:

- Core types
- Payment utilities
- Anchor workflow helpers
- Escrow utilities
- Diagnostics modules
- Validation helpers
- Configuration tools

Package code should be reusable, tested, and clearly scoped.

    </td>
  </tr>
  <tr>
    <td width="50%">

### Contracts

The `contracts/` directory contains smart contract or protocol-related code.

Contract contributions should prioritise:

- Correctness
- Security
- Clear state handling
- Strong tests
- Safe error handling
- Documentation for public behaviour

    </td>
    <td width="50%">

### Examples

The `examples/` directory contains sample implementations and usage references.

Examples should be:

- Easy to understand
- Safe to run locally
- Free from real secrets
- Aligned with current package APIs
- Useful for contributors and integrators

    </td>
  </tr>
</table>

---

## Documentation

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

| Test Type | Purpose |
|---|---|
| Unit tests | Validate small isolated behaviours |
| Integration tests | Validate multiple modules working together |
| Regression tests | Protect existing behaviour during refactors |
| Error-path tests | Confirm failures are handled safely |
| Configuration tests | Validate setup and config behaviour |
| Contract tests | Validate smart contract behaviour |
| Cross-package tests | Confirm packages work together |

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

> Large unscoped changes make review harder. Keep pull requests focused.

---

## Error Handling

Error handling should be consistent and developer-friendly.

Avoid:

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

| Area | Examples |
|---|---|
| Tests | Add regression tests, edge-case tests, or integration tests |
| Refactoring | Clean module boundaries and remove duplicated logic |
| Documentation | Improve setup guides, examples, and architecture notes |
| Diagnostics | Improve validation, reporting, and troubleshooting |
| Contracts | Improve safety, tests, and documentation |
| Developer Experience | Improve scripts, package structure, and local workflow |

Please avoid low-effort changes that do not meaningfully improve the project.

---

## Maintainer Notes

Maintainers should review contributions based on:

| Review Area | What To Check |
|---|---|
| Issue alignment | Does the PR solve the linked issue? |
| Correctness | Does the implementation work as intended? |
| Tests | Are relevant behaviours covered? |
| Code quality | Is the implementation clean and maintainable? |
| Documentation | Are docs updated where needed? |
| Security | Does the change introduce risk? |
| Long-term value | Does this improve the project meaningfully? |

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

```txt
https://github.com/Axionvera
```

---

<div align="center">

## Build With AnchorKit

Explore the codebase.  
Run the tests.  
Pick a meaningful issue.  
Help improve the project.

<br />

**AnchorKit is built for maintainable infrastructure and open contribution.**

</div>