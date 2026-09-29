# NuPhy PRD Clarifier privacy addendum — publication draft

Effective date: to be set when this addendum is published.

NuPhy PRD Clarifier is a skills-only plugin. It does not operate a NuPhy-hosted MCP server, require user authentication, access a NuPhy account, or send conversation content to NuPhy or another third party through plugin-provided code.

Information entered by a user is processed within the OpenAI product the user is using and is subject to the applicable OpenAI account, workspace, and data-control terms. The plugin instructs the model to use that information only to clarify a request and draft a requirement entry and PRD in the current conversation.

Users should not enter passwords, API keys, payment information, customer personal data, confidential financial data, or other secrets. If such information is provided, the plugin is designed to ask the user to redact it and omit it from the draft.

The plugin itself does not set cookies, perform analytics, maintain a user profile, or retain an independent copy of user inputs or generated drafts. NuPhy's general privacy policy remains available at https://nuphy.com/pages/privacy-policy.

Privacy questions may be sent to service@nuphy.com.

Before public submission, NuPhy should have legal counsel approve this addendum and publish it at a stable HTTPS URL under a NuPhy-controlled domain. The listing and manifest should then use that plugin-specific URL.
