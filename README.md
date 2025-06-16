# ForgeCode.dev Agent Personas

<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/images/logo-light.svg">
    <source media="(prefers-color-scheme: light)" srcset="./assets/images/logo-dark.svg">
    <img alt="ForgeCode.dev Logo" src="./assets/images/logo-light.svg" width="200" height="auto">
  </picture>
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
  [![YAML](https://img.shields.io/badge/Config-YAML-blue.svg)](https://yaml.org/)
  [![ForgeCode](https://img.shields.io/badge/Platform-ForgeCode.dev-purple.svg)](https://forgecode.dev)
</div>

## Overview

This repository contains the agent persona configurations for the **ForgeCode.dev** project. Each agent is defined using YAML configuration files that follow the Forge schema format, specifying their system prompts, capabilities, and interaction patterns for AI-powered development assistance.

## Repository Structure

```
.
├── README.md                 # This file
├── LICENSE                   # MIT License
├── assets/                   # Images and media files
│   └── images/              # Logo and icon files
├── agents/                   # Agent configurations
│   ├── lovable/             # Frontend Development Agent
│   │   ├── config.yaml      # Agent configuration
│   │   └── README.md        # Agent documentation
│   └── sage/                # Codebase Analysis Agent
│       ├── config.yaml      # Agent configuration
│       └── README.md        # Agent documentation
```

## Available Agents

### Lovable - Frontend Development Specialist

**Specialization**: React & Modern Frontend Technologies  
**Personality**: Friendly and encouraging  
**Focus**: UI/UX, Performance, Modern tooling

[Learn more about Lovable →](./agents/lovable/README.md)

---

### Sage - Codebase Analysis Expert

**Specialization**: Code Analysis & Understanding  
**Personality**: Analytical and thorough  
**Focus**: Codebase comprehension, code breakdown, detailed analysis

[Learn more about Sage →](./agents/sage/README.md)

---

## Configuration Schema

Each agent configuration follows the Forge schema format:

```yaml
# yaml-language-server: $schema=https://raw.githubusercontent.com/antinomyhq/forge/refs/heads/main/forge.schema.json
templates: 
 - repomix-output.xml
agents:
  - id: "agent_id"
    title: "Agent Title"
    description: |-
      Multi-line description of the agent's purpose
      and capabilities.
    system_prompt: |-
      Detailed system prompt that defines the agent's behavior,
      capabilities, and interaction patterns. This includes:
      
      - Core responsibilities and expertise areas
      - Technical capabilities and preferences
      - Communication style and personality
      - Task approach and methodology
      - Best practices and guidelines
      
      The system prompt uses Handlebars templates for dynamic content:
      {{> forge-partial-system-info.hbs }}
      {{> forge-partial-tool-information.hbs }}
      
      {{#if custom_rules}}
      <custom_rules>
      {{custom_rules}}
      </custom_rules>
      {{/if}}
    user_prompt: <task>{{event.value}}</task>
```

## Getting Started

### Adding a New Agent

1. **Create Agent Directory**

   ```bash
   mkdir agents/new-agent-name
   cd agents/new-agent-name
   ```

2. **Create Configuration File**

   ```bash
   touch config.yaml
   ```

3. **Define Agent Persona**
   Use the schema above to define your agent's capabilities and personality.

4. **Add Documentation**
   ```bash
   touch README.md
   ```

### Using Agent Configurations

These configurations are designed to be consumed by the ForgeCode.dev platform to instantiate AI agents with specific personas and capabilities. The Forge platform uses these YAML files to:

- Load agent-specific system prompts and behavior patterns
- Apply the appropriate templates and context information
- Configure the agent's interaction style and technical focus
- Enable specialized development assistance for different domains

```yaml
# Example usage in ForgeCode.dev
agent_config:
  source: "agent-configs/agents/lovable/config.yaml"
  agent_id: "lovable"
  task: "create_react_component"
  parameters:
    component_name: "UserProfile"
    styling: "shadcn"
    typescript: true
```

## Configuration Guidelines

### Best Practices

- **Consistency**: Use consistent naming conventions across all agent configs
- **Schema Compliance**: Follow the Forge schema format for compatibility
- **Documentation**: Include comprehensive descriptions and examples
- **Validation**: Ensure YAML syntax is valid before committing
- **Template Usage**: Leverage Handlebars templates for dynamic content

### Required Fields

- `templates`: List of template files to include (typically `repomix-output.xml`)
- `agents`: Array of agent configurations
- `agents[].id`: Unique identifier for the agent
- `agents[].title`: Human-readable agent name
- `agents[].description`: Brief description of agent purpose and capabilities
- `agents[].system_prompt`: Comprehensive prompt defining agent behavior and capabilities
- `agents[].user_prompt`: Template for user input processing

### Optional Fields

- Schema validation: `yaml-language-server` directive for IDE support
- Custom rules: Conditional logic in system prompts using Handlebars
- Additional templates: Custom template files beyond the standard ones

## Contributing

### Adding New Agents

1. Fork this repository
2. Create a new branch for your agent
3. Follow the configuration schema
4. Add comprehensive documentation
5. Submit a pull request

### Modifying Existing Agents

1. Update the configuration file
2. Update documentation if needed
3. Test the configuration with the Forge platform
4. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Related Projects

- [ForgeCode.dev Platform](https://forgecode.dev) - Main platform
- [ForgeCode.dev Documentation](https://forgecode.dev/docs) - Platform documentation
- [ForgeCode.dev App](https://app.forgecode.dev) - Platform application

---

<div align="center">
  <img src="./assets/images/favicon-light.svg" alt="ForgeCode.dev" width="24" height="24">
  
  **Built with ❤️ for the ForgeCode.dev ecosystem**
</div>
