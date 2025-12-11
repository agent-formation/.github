# Agentic Spec

**Open standard for declarative AI agent systems.**

Define your agents, tools, and multi-agent orchestration in portable YAML. Run them on any compliant runtime.

---

## Why Agentic Spec?

AI agent configurations are fragmented. Every framework has its own format, locking you into a specific runtime. Agentic Spec changes that:

- **Write once** - Declarative YAML schemas for agents, MCP tools, and A2A services
- **Run anywhere** - Portable across any compliant runtime
- **Validate consistently** - Standard tooling for linting and validation
- **Extend safely** - Namespaced extensions for vendor-specific features

Think of it as **infrastructure-as-code for AI agents**.

---

## The Formation Standard

A **Formation** is a complete AI agent system defined in YAML:

```yaml
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

---

## Projects

| Repository | Description |
|------------|-------------|
| [**formation**](https://github.com/agentic-spec/formation) | Core schemas, specs, and templates |
| *validator* | Schema validation library (coming soon) |
| *linter* | CLI linting tool (coming soon) |
| *vscode* | VS Code extension (coming soon) |

---

## Get Started

```bash
# Clone the formation templates
git clone https://github.com/agentic-spec/formation.git
cp -r formation/formation my-project
cd my-project

# Customize and deploy with any compliant runtime
```

---

## Implementations

- [**MUXI**](https://github.com/muxi-ai/muxi) - Reference implementation

Building a runtime? We'd love to list it. Open an issue or PR.

---

## Contributing

Agentic Spec is developed in the open. We welcome contributions to schemas, specs, tooling, and documentation.

- Read the [Contributing Guide](https://github.com/agentic-spec/formation/blob/main/CONTRIBUTING.md)
- Review the [Governance Model](https://github.com/agentic-spec/formation/blob/main/GOVERNANCE.md)
- Join the discussion in [Issues](https://github.com/agentic-spec/formation/issues)

---

## License

Apache License 2.0

---

<p align="center">
  <i>Portable agents. Open standard. Community driven.</i>
</p>
