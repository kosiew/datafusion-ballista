# Gemini Guidelines for the Ballista Project

This document provides context and guidelines for using Gemini to assist with development in the Ballista project.

## Project Overview

Ballista is a distributed query execution engine built on Apache DataFusion. It is written in Rust and uses Apache Arrow as its in-memory format. The goal of Ballista is to provide a distributed query engine that can be used to execute DataFusion query plans in a cluster of executors.

The project is composed of several crates:

-   `ballista`: The main crate, which contains the Ballista library.
-   `ballista-cli`: A command-line interface for interacting with a Ballista cluster.
-   `ballista/core`: Core data structures and utilities.
-   `ballista/scheduler`: The Ballista scheduler, which is responsible for receiving queries from clients, creating a distributed query plan, and scheduling tasks across available executors.
-   `ballista/executor`: The Ballista executor, which is responsible for executing a partition of a query.

## Key Technologies

-   **Language:** Rust
-   **Build Tool & Package Manager:** Cargo
-   **CI/CD:** GitHub Actions
-   **Containerization:** Docker and Docker Compose

## Development Workflow

### Common Commands

-   **Build:** `cargo build`
-   **Test:** `cargo test`
-   **Lint:** `./dev/rust_lint.sh` or `cargo clippy`
-   **Format:** `cargo fmt`
-   **Run Integration Tests:** `./dev/integration-tests.sh`
-   **Build Docker Images:** `./dev/build-ballista-docker.sh`

### Coding Style

The project follows standard Rust conventions and uses `rustfmt` for code formatting and `clippy` for linting. Please adhere to the existing coding style and conventions when making changes.

### Commits and Pull Requests

Commits should be atomic and focus on a single logical change. Pull requests should be well-documented and include a clear description of the changes made.

## Project Structure

-   `.github/`: GitHub Actions workflows and issue templates.
-   `ballista/`: The main Ballista crates.
-   `ballista-cli/`: The Ballista command-line interface.
-   `benchmarks/`: Benchmarking code.
-   `ci/`: Scripts for CI/CD.
-   `dev/`: Scripts for development tasks.
-   `docs/`: Project documentation.
-   `examples/`: Example usage of Ballista.
-   `python/`: Python bindings for Ballista.
