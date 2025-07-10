# Repository Guidelines for Codex Agents

This repository contains the Ballista project, which is written mostly in Rust.
Follow the steps below before submitting any pull request.

## Required Checks

- **Rust formatting and linting**
  - Format code with `cargo fmt` using `ci/scripts/rust_fmt.sh`.
  - Run Clippy using `ci/scripts/rust_clippy.sh`.
  - Ensure `Cargo.toml` files are formatted using `ci/scripts/rust_toml_fmt.sh`.
  - You can run all of these together with `./dev/rust_lint.sh`.
- **Tests**
  - Run `cargo test` for the workspace.
  - Integration tests can be executed with `./dev/integration-tests.sh` if needed (requires Docker).
- **Documentation**
  - Format Markdown files with Prettier as described in `CONTRIBUTING.md`.

## Commits

Keep commits focused and descriptive. Each commit should represent a single logical change.
