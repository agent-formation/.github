<p align="center">
<img src="https://avatars.githubusercontent.com/u/249095986?v=1" width="112" height="112">
</p>

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

Agents, tools, memory, knowledge, workflows - all declared, all portable.

> **File Extensions:** Use `.afs` (Agent Formation Schema) or `.yaml` - both are fully supported.

---

## Projects

| Repository | Description |
|------------|-------------|
| [**afs-spec**](https://github.com/agent-formation/afs-spec) | Core schemas, specs, and templates |
| [**afs-cli**](https://github.com/agent-formation/afs-cli) | Validator, linter, and formatter tool |
| [**afs-vscode**](https://github.com/agent-formation/afs-vscode) | VS Code extension |
| [**afs-assets**](https://github.com/agent-formation/afs-assets) | Logos, icons, badges, and brand guidelines |

---

## Get Started

```bash
# Clone the formation templates
git clone https://github.com/agent-formation/afs-spec.git
cp -r afs-spec/schemas my-project
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

- Read the [Contributing Guide](https://github.com/agent-formation/afs-spec/blob/main/CONTRIBUTING.md)
- Review the [Governance Model](https://github.com/agent-formation/afs-spec/blob/main/GOVERNANCE.md)
- Join the discussion in [Issues](https://github.com/agent-formation/afs-spec/issues)

---

## License

Apache License 2.0

---

<p align="center">
  <i>Portable agents. Open standard. Community driven.</i>
</p>
