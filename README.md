# Agent Memory MCP Skill

A Claude skill for working with persistent agent memory through a Model Context Protocol (MCP) server. The skill describes a memory-bank workflow that allows an agent to search existing knowledge, save new information, retrieve specific records, and inspect memory usage.

## What This Skill Covers

- Setting up the agent memory project and its Node.js dependencies.
- Starting the MCP server for a target workspace.
- Searching memories by query, type, and tags.
- Writing durable decisions, patterns, and project knowledge.
- Reading a saved memory by its key.
- Viewing memory statistics and using the included dashboard.

## Repository Structure

- `SKILL.md`: Original skill instructions, setup steps, MCP tool descriptions, and dashboard usage.
- `LICENSE`: MIT License for this repository.

## Prerequisites

The documented setup requires Node.js 18 or newer and npm. Review the setup commands in `SKILL.md` and confirm the memory project is installed in the intended workspace before starting the server.

## Typical Workflow

1. Install dependencies and compile the memory project.
2. Start the MCP server with a project identifier and absolute workspace path.
3. Search existing memories before making decisions that may already be documented.
4. Write useful, durable information with meaningful keys, types, and tags.
5. Retrieve stored entries when a task needs prior decisions or project context.
6. Use the dashboard when a visual overview of memory usage is helpful.

## Usage

Add the skill to a Claude-compatible environment that supports MCP integrations. Use it when implementing or operating persistent memory for an AI agent. The repository contains the skill instructions, not a bundled copy of the external memory server.

## License

Released under the MIT License. See [LICENSE](LICENSE) for details.
