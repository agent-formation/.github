# Agent Formation
**Open standard for declarative AI agent systems.**

Define your agents, tools, and multi-agent orchestration in portable AFS files. Run them on any compliant runtime.

---

## Why Agent Formation?

AI agent configurations are fragmented. Every framework has its own format, locking you into a specific runtime. Agent Formation changes that:

- **Write once** - Declarative schemas for agents, MCP tools, and A2A services
- **Run anywhere** - Portable across any compliant runtime
- **Validate consistently** - Standard tooling for linting and validation
- **Extend safely** - Namespaced extensions for vendor-specific features

Think of it as **infrastructure-as-code for AI agents**.

---

## The Formation Schema

A **Formation** is a complete AI agent system defined in AFS (or YAML):

```yaml
# formation.afs
schema: "1.0.0"
id: my-formation
description: Customer support system

llm:
  models:
    - text: openai/gpt-4o

agents:
  - id: support-agent
    role: Customer Support
    tools: [knowledge-base, ticketing]

mcp:
  - id: knowledge-base
    command: npx @company/kb-server
```

Agents, tools, memory, knowledge, secrets - all declared, all portable.

> **File Extensions:** Use `.afs` (Agent Formation Schema) or `.yaml` - both are fully supported.

---

## Projects

| Repository | Description |
|------------|-------------|
| [**spec**](https://github.com/agent-formation/spec) | Core schemas, specs, and templates |
| *validator* | Schema validation library (coming soon) |
| *linter* | CLI linting tool (coming soon) |
| *vscode* | VS Code extension (coming soon) |

---

## Get Started

```bash
# Clone the formation templates
git clone https://github.com/agent-formation/spec.git
cp -r spec/formation my-project
cd my-project

# Customize and deploy with any compliant runtime
```

---

## Implementations

- [**MUXI**](https://github.com/muxi-ai/muxi) - Reference implementation

Building a runtime? We'd love to list it. Open an issue or PR.

---

## Contributing

Agent Formation is developed in the open. We welcome contributions to schemas, specs, tooling, and documentation.

- Read the [Contributing Guide](https://github.com/agent-formation/spec/blob/main/CONTRIBUTING.md)
- Review the [Governance Model](https://github.com/agent-formation/spec/blob/main/GOVERNANCE.md)
- Join the discussion in [Issues](https://github.com/agent-formation/spec/issues)

---

## License

Apache License 2.0

---

<p align="center">
  <i>Portable agents. Open standard. Community driven.</i>
</p>
