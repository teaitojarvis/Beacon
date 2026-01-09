# Threat Model

Beacon is a governance layer for personal AI agents. This document highlights key risks and mitigation principles.

## Threats in scope

- **Prompt injection / tool injection**
  - Agents or tools receive adversarial instructions that bypass approval intent.
- **Data exfiltration**
  - Sensitive data is extracted via tools, logs, or side channels.
- **Supply-chain risk**
  - Dependency compromise, poisoned updates, or malicious packages.
- **Sandbox escape**
  - Execution breaks out of constraints to reach host resources.
- **Logs and PII leakage**
  - Over-collection or unsafe storage of personal data.

## Mitigation principles

- **Explicit consent gates** before any action with external side effects.
- **Least privilege** for tools, capabilities, and data access.
- **Observable execution** with structured logs and evidence trails.
- **Local-first defaults** to minimize data exposure.
- **Dependency hygiene** with pinning, review, and minimal surface area.
- **Isolation boundaries** that assume tools and prompts can be hostile.
