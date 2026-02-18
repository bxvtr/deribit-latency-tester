# Contributing

Thank you for contributing to **Deribit Latency Tester**.

This project focuses on precise, reproducible measurement of WebSocket RPC latency within the Deribit trading system. Contributions should emphasize measurement accuracy, deterministic behavior, clean async design, and transparent analytics.

The objective is a lightweight tool that produces realistic latency profiles without hidden logic or unintended side effects.

---

## Design Principles

All changes must align with the following principles:

- Deterministic and reproducible timing behavior
- Strict separation between networking, measurement logic, and reporting
- No hidden state or implicit retry mechanisms
- Correctness over convenience
- Explicit and predictable failure handling

Avoid introducing magic defaults, uncontrolled concurrency, silent recovery logic, or non-transparent abstractions.

---

## Contribution Workflow

1. Fork the repository
2. Create a focused feature or fix branch
3. Keep commits small and logically scoped
4. Open a Pull Request with a clear technical description

The Pull Request should clearly describe:

- Motivation
- Architectural or measurement changes
- Impact on latency precision, determinism, or stability

---

## Commit Conventions

Use concise and technically descriptive commit messages:

feat: add tick-aligned latency correlation
fix: handle websocket close edge case
perf: reduce timestamp allocation overhead
docs: clarify config.toml parameters

---

## Development Setup

Recommended environment:

- Rust stable toolchain
- VS Code Devcontainer (included)

Manual setup:

```bash
cargo build
```

Optional formatting and linting:

```bash
cargo fmt
cargo clippy
```

---

## Testing & Validation

Before submitting a Pull Request:

- The project must build without warnings
- CI must pass reproducibly
- New logic must not silently alter existing latency measurements

If new metrics or timing paths are introduced, documentation must clearly explain how they are measured and interpreted.
