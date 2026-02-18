# Security Policy

## Supported Versions

Only the latest state of the `main` branch is actively maintained.

Earlier commits, historical versions, and forks may not receive security fixes
or vulnerability patches.

---

## Reporting a Vulnerability

If a security issue is identified, **do not open a public GitHub issue**.

Instead, report responsibly using one of the following channels:

- GitHub Security Advisories
- Direct contact with the repository maintainer via GitHub

A vulnerability report should include:

- A clear technical description of the issue
- Steps to reproduce, if applicable
- Affected modules, files, or RPC flows
- Potential impact (data exposure, order manipulation, denial of service, etc.)

All reports are handled through responsible disclosure practices.

---

## Security Scope

This repository provides a Rust-based tool for interacting with the Deribit WebSocket API and measuring RPC latency, including:

- WebSocket connection handling
- Authenticated RPC request flows
- Order lifecycle actions (open, edit, cancel)
- Timestamp collection and latency analysis
- CSV logging and statistical summaries

Primary security considerations include:

- API credential handling via environment variables
- WebSocket message integrity and validation
- Safe file output for measurement data
- Dependency vulnerabilities in async/networking crates

---

## Dependency Security

- Dependencies are explicitly defined in `Cargo.toml`
- The Rust stable toolchain is targeted
- Security-related dependency updates are prioritized

CI is expected to catch build and compatibility issues.

---

## Responsible Usage

Users are responsible for:

- Secure storage of API credentials
- Avoiding credential exposure in logs or output files
- Operating within Deribit API rate limits and policies
- Running the tool in secure environments

This project does not manage account permissions, API key scopes, or infrastructure security.

---

## Disclosure Policy

Allow reasonable time for investigation and remediation before any public
disclosure of reported security vulnerabilities.
