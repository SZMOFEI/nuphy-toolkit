# NuPhy Toolkit

[English](README.md) | [简体中文](README.zh-CN.md)

An extensible AI workflow toolkit for NuPhy teams. Its first capability turns vague operational requests into structured, Feishu-ready requirement entries and lightweight PRD drafts through focused clarification.

NuPhy Toolkit follows a simple model: one shared plugin containing multiple focused Skills. New capabilities are added only after a real, repeated workflow has been validated. The current release provides requirement clarification and PRD drafting only; it does not change code, write to Feishu, contact engineering teams, or publish changes.

## What it does

- Clarifies ambiguous requests through focused, step-by-step questions.
- Reviews existing requirements and identifies missing information.
- Produces an immediate draft with explicit gaps and assumptions when the user wants to skip the interview.
- Generates a Feishu-ready requirement entry and lightweight PRD draft.
- Separates known facts, missing information, and assumptions requiring confirmation.
- Uses Chinese by default and can produce English output on request.

## Install from GitHub

You need a version of the ChatGPT desktop app or Codex CLI that supports plugins.

### Option 1: Add the GitHub marketplace directly

```bash
codex plugin marketplace add SZMOFEI/nuphy-toolkit
codex plugin add nuphy-toolkit@nuphy-open-plugins
```

Start a new chat after installation so the new Skill is loaded.

### Option 2: Install from a downloaded ZIP

1. Select **Code → Download ZIP** in this GitHub repository and extract it.
2. Run:

```bash
codex plugin marketplace add /absolute/path/to/nuphy-toolkit
codex plugin add nuphy-toolkit@nuphy-open-plugins
```

Replace `/absolute/path/to/nuphy-toolkit` with the absolute path to the extracted repository.

### Check for updates

```bash
codex plugin marketplace list
codex plugin marketplace upgrade nuphy-open-plugins
```

After upgrading, reinstall the plugin and start a new chat:

```bash
codex plugin add nuphy-toolkit@nuphy-open-plugins
```

## Example prompts

- `Help me clarify this vague request into a requirement card ready for review.`
- `Fill in this operational request step by step and produce a PRD draft.`
- `Review this requirement for missing information and return a Feishu-ready version.`
- `Stop asking questions and draft it now using the available information.`

## Current outputs

1. Feishu-ready requirement entry
2. Lightweight PRD draft
3. Missing information
4. Assumptions requiring confirmation

## Privacy and permissions

- No NuPhy, Feishu, or other third-party account is required.
- The current release contains no MCP server and sends no conversation data to NuPhy servers.
- It does not read local files unless the user provides them in the current conversation.
- Do not provide passwords, API keys, payment information, customer personal data, or other secrets.

## Repository structure

```text
.agents/plugins/marketplace.json
plugins/nuphy-toolkit/
├── plugin.json
├── .codex-plugin/plugin.json
├── assets/
├── skills/
├── submission/
└── tests/
```

## Development and validation

The plugin source is in `plugins/nuphy-toolkit`. Keep each capability in an independently triggered and testable Skill, and add new capabilities only after their practical value has been validated. Before submitting changes, run the OpenAI `skill-creator` and `plugin-creator` validators and confirm that the relevant behavioral tests still pass.

## License

MIT
