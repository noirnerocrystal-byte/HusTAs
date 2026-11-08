# Security

HusTAs is a local-first desktop application that may optionally connect to user-selected external AI, search, or vision services.

## Safe use

- Use releases obtained from the project's official distribution surface.
- Do not expose a HusTAs instance directly to the public internet. Treat local/LAN access as access to a private application, not as a hardened public web service.
- Treat local application data, credentials, logs, backups, workspace metadata, and diagnostic bundles as sensitive. Do not post them publicly.
- External providers have their own security, privacy, account, and billing policies. Only connect services you intend to use.
- A compromised Windows account or host machine can compromise locally stored application data; HusTAs is not intended to provide a second security boundary against a fully compromised host.

## Workspace isolation

Workspace file access is scoped to the local directory explicitly selected by the Developer.

Security expectations for workspace file access include:

- ordinary chats do not receive workspace filesystem access;
- file requests are resolved relative to the authorized workspace root;
- traversal outside that root is rejected;
- absolute-path and cross-workspace access attempts are rejected;
- symlink / reparse-point escapes outside the authorized root are rejected;
- deleting a workspace does not delete the host's actual files;
- workspace access does not imply shell access, Python execution, Computer Use, or unrestricted host filesystem access.

A workspace should be treated as permission to use the selected directory for that workspace only, not as general permission to inspect or modify the host filesystem.

Workspace isolation is an application-level access-control boundary. It is not an operating-system security sandbox and is not intended to protect data from a process or user account that already has broader access to the host system.

## Application roles

Administrative functions are restricted to the Developer role.

Developer-only capabilities include:

- group creation and deletion;
- group membership management;
- workspace creation, deletion, and directory authorization;
- memory organization / management.

Ordinary users may:

- privately chat with AI agents;
- participate in conversations they have been invited to;
- view shared-screen activity available to those conversations.

Ordinary users do not receive group-management, workspace-management, filesystem-authorization, or memory-management controls.

Server-side authorization remains the enforcement boundary; hiding a control in the UI is not treated as sufficient authorization by itself.

## Shared-screen activity

Shared-screen activity is view / context sharing, not Computer Use.

HusTAs does not grant AI participants mouse control, keyboard control, remote desktop control, or automatic interaction with the user's computer through the shared-screen feature.

## External model connections

Model/provider configuration is validated when the configured model is used. Imported persona configuration may reference a provider that has not yet been configured locally.

Do not assume that a restored or imported provider identifier means the external connection has already been authenticated or verified.

## Reporting a security issue

Do not publish credentials, private user data, local-file contents, or actionable exploit details in a public issue.

If no private reporting channel is listed for the current release, open only a minimal public issue stating that you need a private security contact, without including exploit details.
