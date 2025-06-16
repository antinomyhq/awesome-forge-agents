# 🤖 ForgeCode.dev Agent Personas

<div align="center">
  <img src="./assets/images/logo-light.svg" alt="ForgeCode.dev Logo" width="200" height="auto">
  
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
  [![YAML](https://img.shields.io/badge/Config-YAML-blue.svg)](https://yaml.org/)
  [![ForgeCode](https://img.shields.io/badge/Platform-ForgeCode.dev-purple.svg)](https://forgecode.dev)
</div>

## 📋 Overview

This repository contains the agent persona configurations for the **ForgeCode.dev** project. Each agent is defined using YAML configuration files that specify their capabilities, personality traits, technical preferences, and workflow settings.

## 🏗️ Repository Structure

```
agent-configs/
├── README.md                 # This file
├── lovable/                  # Frontend Development Agent
│   ├── config.yaml          # Agent configuration
│   └── README.md            # Agent documentation
└── sage/                    # Backend Architecture Agent
    ├── config.yaml          # Agent configuration
    └── README.md            # Agent documentation
```

## 🤖 Available Agents

### 💖 Lovable - Frontend Development Specialist
<img src="./assets/images/logo-small-light.png" alt="Lovable Agent" width="32" height="32" align="left">

**Specialization**: React & Modern Frontend Technologies  
**Personality**: Friendly and encouraging  
**Focus**: UI/UX, Performance, Modern tooling

[📖 Learn more about Lovable →](./lovable/README.md)

---

### 🧙‍♂️ Sage - Backend Architecture Expert
<img src="./assets/images/logo-small-dark.png" alt="Sage Agent" width="32" height="32" align="left">

**Specialization**: System Architecture & Backend Development  
**Personality**: Thoughtful and analytical  
**Focus**: Scalability, Security, Performance

[📖 Learn more about Sage →](./sage/README.md)

---

## 🛠️ Configuration Schema

Each agent configuration follows a standardized YAML schema:

```yaml
name: "Agent Name"
version: "1.0.0"
description: "Agent description"

agent:
  type: "agent_type"
  specialization: "specialization_area"

capabilities:
  - "capability_1"
  - "capability_2"

personality:
  communication_style: "style"
  expertise_level: "level"
  problem_solving_approach: "approach"

preferences:
  # Technology preferences

workflow:
  # Workflow settings

integrations:
  # Integration configurations
```

## 🚀 Getting Started

### Adding a New Agent

1. **Create Agent Directory**
   ```bash
   mkdir new-agent-name
   cd new-agent-name
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

These configurations are designed to be consumed by the ForgeCode.dev platform to instantiate AI agents with specific personas and capabilities.

```yaml
# Example usage in ForgeCode.dev
agent_config:
  source: "agent-configs/lovable/config.yaml"
  task: "create_react_component"
  parameters:
    component_name: "UserProfile"
    styling: "tailwind"
```

## 📊 Agent Comparison

| Feature | Lovable | Sage |
|---------|---------|------|
| **Primary Focus** | Frontend Development | Backend Architecture |
| **Communication Style** | Friendly & Encouraging | Thoughtful & Analytical |
| **Expertise Level** | Expert | Senior Architect |
| **Main Technologies** | React, TypeScript, Tailwind | Python, Go, PostgreSQL |
| **Problem Solving** | Iterative & Collaborative | Systematic & Thorough |

## 🔧 Configuration Guidelines

### Best Practices

- **Consistency**: Use consistent naming conventions across all agent configs
- **Versioning**: Always specify version numbers for tracking changes
- **Documentation**: Include comprehensive descriptions and examples
- **Validation**: Ensure YAML syntax is valid before committing

### Required Fields

- `name`: Human-readable agent name
- `version`: Semantic version number
- `description`: Brief description of agent purpose
- `agent.type`: Agent category/type
- `capabilities`: List of agent capabilities
- `personality`: Personality traits and communication style

### Optional Fields

- `preferences`: Technology and tool preferences
- `workflow`: Workflow-specific settings
- `integrations`: External tool integrations

## 🤝 Contributing

### Adding New Agents

1. Fork this repository
2. Create a new branch for your agent
3. Follow the configuration schema
4. Add comprehensive documentation
5. Submit a pull request

### Modifying Existing Agents

1. Update the configuration file
2. Increment the version number
3. Update documentation if needed
4. Test the configuration
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Related Projects

- [ForgeCode.dev Platform](https://forgecode.dev) - Main platform
- [ForgeCode.dev Documentation](https://docs.forgecode.dev) - Platform documentation
- [ForgeCode.dev API](https://api.forgecode.dev) - Platform API

---

<div align="center">
  <img src="./assets/images/favicon-light.svg" alt="ForgeCode.dev" width="24" height="24">
  
  **Built with ❤️ for the ForgeCode.dev ecosystem**
</div>