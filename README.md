# claude-agent-memory-mcp-skill

A Claude Code skill for integrating persistent, searchable project memory into AI agents through a Model Context Protocol (MCP) server.

## Overview

This skill describes a memory-bank workflow for storing durable project knowledge and retrieving it across tasks. It focuses on architecture decisions, implementation patterns, project conventions, and other information that remains useful beyond a single conversation.

Memory should be selective. Store information that will improve future work, not every transient detail.

## Main Capabilities

- Set up a persistent memory service.
- Start an MCP server for a workspace.
- Search memories using queries, types, and tags.
- Write durable knowledge with stable keys.
- Retrieve specific memory records.
- Inspect memory usage and statistics.
- Use the included dashboard where configured.
- Organize project knowledge for reuse across agent sessions.

## Prerequisites

The documented setup expects:

- Node.js 18 or newer.
- npm.
- The memory project installed in the intended workspace.
- A Claude-compatible MCP environment.

Review the setup steps in `SKILL.md` before compiling or starting the server.

## Installation

Clone the skill:

```bash
git clone https://github.com/Brajesh31/claude-agent-memory-mcp-skill.git ~/.claude/skills/agent-memory-mcp
```

The MCP memory server is a separate project and must be installed and configured independently.

## Usage

Invoke the skill when implementing or operating persistent agent memory:

```text
/agent-memory-mcp
```

Provide the workspace, memory categories, retrieval needs, and retention expectations.

## Typical Workflow

1. Install the memory service and dependencies.
2. Build or compile the service as required.
3. Configure the MCP server for the target workspace.
4. Search existing memory before making decisions.
5. Save only durable and useful information.
6. Use consistent keys, types, and tags.
7. Retrieve relevant records during future tasks.
8. Review memory quality and remove stale information through the supported workflow.

## Memory Design Guidelines

- Prefer concise, factual records.
- Separate decisions from temporary task notes.
- Include enough context to understand why a decision was made.
- Use stable keys and consistent categories.
- Avoid storing secrets or unnecessary personal information.
- Update outdated records rather than accumulating contradictory entries.
- Keep project-specific memories scoped to the correct workspace.

## Repository Contents

- `SKILL.md`: Main memory setup and MCP workflow instructions.
- `README.md`: Capabilities, prerequisites, and memory design guidance.

## Security Considerations

Memory can persist sensitive information beyond the current task. Define access boundaries, filesystem permissions, backup behavior, and retention rules. Do not store API keys, passwords, private keys, or confidential data unless the system has an explicitly approved secure handling design.

## Validation Checklist

- MCP server starts successfully.
- The intended workspace is configured.
- Search returns relevant records.
- Writes persist across sessions.
- Memory keys and tags are consistent.
- Sensitive data is excluded.
- Stale information can be identified and updated.

## Practical Principle

Persistent memory should reduce repeated explanation and preserve useful decisions. If a record is unlikely to change future work, it probably does not need to be stored.
