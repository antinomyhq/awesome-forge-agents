# Lovable Agent

## Overview

Lovable is a specialized AI editor that creates and modifies web applications with real-time preview capabilities. It specializes in React, TypeScript, and modern frontend technologies with a strong focus on UI/UX excellence and best practices.

## Key Features

- **Real-time Development**: AI editor that makes code changes while users see live preview in an iframe
- **React & TypeScript Expertise**: Deep knowledge of React patterns, TypeScript integration, and modern frontend development
- **Component-Driven Development**: Creates small, focused components following atomic design principles
- **Modern Tooling**: Proficient with Vite, shadcn/ui, React Query, and contemporary build tools
- **Performance Optimization**: Implements code splitting, optimized image loading, and minimizes re-renders
- **Security-First**: Validates inputs, implements proper authentication flows, and follows OWASP guidelines
- **Testing & Documentation**: Writes comprehensive tests and maintains clear documentation
- **Responsive Design**: Implements mobile-first, responsive designs by default

## Core Principles

### Code Quality & Organization

- Small, focused components (< 50 lines)
- TypeScript for type safety
- Extensive console logging for debugging
- Proper file organization and structure

### State Management

- React Query for server state
- Local state with useState/useContext
- Avoids prop drilling
- Implements response caching

### Error Handling

- Toast notifications for user feedback
- Proper error boundaries
- User-friendly error messages
- Comprehensive error logging

## Usage Examples

### Component Development

```yaml
task: "create_component"
component_type: "functional"
styling: "shadcn"
typescript: true
responsive: true
```

### Feature Implementation

```yaml
task: "implement_feature"
feature: "user_authentication"
framework: "react"
state_management: "react_query"
ui_library: "shadcn"
```

### Performance Optimization

```yaml
task: "optimize_performance"
focus: "code_splitting"
target: "reduce_bundle_size"
tools: ["vite", "react_lazy"]
```

### Testing Implementation

```yaml
task: "add_tests"
test_type: "integration"
component: "UserProfile"
coverage: "responsive_layouts"
```

## Technical Capabilities

- **Frameworks**: React, Next.js, Vite
- **Languages**: TypeScript, JavaScript, HTML, CSS
- **Styling**: Tailwind CSS, shadcn/ui, CSS Modules
- **State Management**: React Query, useState, useContext
- **Testing**: Unit tests, integration tests, responsive testing
- **Performance**: Code splitting, image optimization, React hooks optimization
- **Security**: Input validation, authentication flows, data sanitization

## Configuration Options

See `config.yaml` for detailed configuration options and customization possibilities.
