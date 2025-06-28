# AI Rules Specification

**Core specification and schema for Universal AI Rules** 📋

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](../LICENSE)
[![Project Status: Concept](https://img.shields.io/badge/Project%20Status-Concept-orange.svg)](https://github.com/Universal-AI-Rules)

## Overview

This package contains the core specification, schema definitions, and validation rules for the Universal AI Rules format (`.ai/ai-rules.yaml`). It defines the standard that all AI coding assistants should follow when reading unified rule files.

## What's Included

> **⚠️ Note: This specification is still being developed. We need contributors to help design and implement it!**

### Planned Components

- **YAML Schema** - JSON Schema definition for `.ai/ai-rules.yaml` format
- **Validation Rules** - Rules for validating rule files
- **Format Specification** - Detailed documentation of the file format
- **Extension Mechanisms** - How to extend the spec for new AI tools
- **Migration Guides** - How to convert from existing formats
- **Best Practices** - Guidelines for writing effective rules

## Schema Structure (Draft)

```yaml
# .ai/ai-rules.yaml
version: "1.0"
project:
  name: string
  description: string
  type: "web" | "api" | "cli" | "library" | "mobile"

rules:
  - name: string
    content: string
    applies_to: string[]
    priority: "low" | "medium" | "high"
    
tools:
  enabled: string[]
  [tool_name]:
    output_path: string
    template: string
    options: object
```

## Supported AI Tools

The specification will define how to generate config files for:

- GitHub Copilot (`.github/copilot-instructions.md`)
- Claude (Anthropic) (`CLAUDE.md`, `CLAUDE.local.md`)
- Cursor (`.cursor/rules/*.md`)
- Windsurf (`.windsurf/rules/*.md`)
- Cline (`.clinerules/*.md`)
- OpenAI Codex & Jules (`AGENTS.md`)
- Aider (`CONVENTIONS.md`)
- Sourcegraph Cody (`.sourcegraph/memory.md`)
- JetBrains AI (`.junie/instructions.md`)

## Get Involved

We need help designing this specification:

- 📝 **Review existing formats** - analyze current AI tool rule formats
- 🔧 **Design the schema** - help create the YAML structure
- ✅ **Build validation** - implement schema validation
- 📚 **Write documentation** - create clear specification docs
- 🧪 **Create examples** - provide sample rule files

## Contributing

This is where the Universal AI Rules project starts. If you're interested in:
- YAML schema design
- JSON Schema validation
- Technical specification writing
- API design

Please contribute! Check out our [main project](../) for contribution guidelines.

## License

MIT License - see [LICENSE](../LICENSE) for details.