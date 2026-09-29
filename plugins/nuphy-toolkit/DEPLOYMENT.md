# NuPhy Toolkit — build and release guide

## Product decision

- **Name:** `nuphy-toolkit`
- **Public display name:** NuPhy Toolkit
- **MVP shape:** skills-only plugin
- **Current Skill:** guided requirement clarification, gap review, Feishu-ready requirement entry, lightweight PRD draft
- **Growth rule:** add focused Skills only after a repeated NuPhy workflow is validated
- **Out of scope:** code changes, publishing, Feishu writes, notifications, final priority, engineering estimates

## Why no API or MCP in v0.1.0

The MVP only transforms information inside the current conversation. A remote service would add authentication, hosting, privacy, tool-schema, domain-verification, and review surface without improving the core user outcome. Add MCP only when NuPhy is ready to read from or write to Feishu under explicit user authorization.

## Local test

This repository includes a marketplace at `.agents/plugins/marketplace.json`. Add the repository as a marketplace, install `nuphy-toolkit`, and test it in a new chat with the prompts in `submission/starter-prompts.md`.

## GitHub distribution

This repository can be installed without public-directory approval:

```bash
codex plugin marketplace add SZMOFEI/nuphy-toolkit
codex plugin add nuphy-toolkit@nuphy-open-plugins
```

Users can also download the repository ZIP and add the extracted directory as a local marketplace. Repository distribution is separate from the universal public Plugins Directory.

Run both validation commands before packaging:

```bash
python3 /path/to/skill-creator/scripts/quick_validate.py skills/nuphy-requirement-clarifier
python3 /path/to/plugin-creator/scripts/validate_plugin.py .
```

## Public submission

1. In the OpenAI Platform organization that will publish the plugin, verify the NuPhy business identity.
2. Confirm the submitter has Apps Management write permission.
3. Create a plugin submission and choose **Skills only**.
4. Upload the final `nuphy-requirement-clarifier` skill bundle.
5. Copy listing details from `submission/listing.json` and upload `assets/icon.png`.
6. Add the three starter prompts and all five positive plus three negative tests.
7. Select only countries and regions supported by NuPhy's legal and support teams.
8. Review and publish the plugin-specific privacy addendum at a stable NuPhy HTTPS URL; update the manifest and listing to that URL before submission.
9. Complete policy attestations, submit for review, address any feedback, then publish after approval.

## Phase 2 interface, not part of this MVP

Only after the conversational workflow proves useful, add a remote MCP server with one narrowly scoped preview-first tool:

```text
create_feishu_requirement_draft
```

The tool should accept the finalized output schema, create a draft rather than silently publishing, use OAuth with minimum Feishu scopes, and be declared as a write action. It must not receive the full chat transcript. A second explicit confirmation should be required before any final Feishu write.
