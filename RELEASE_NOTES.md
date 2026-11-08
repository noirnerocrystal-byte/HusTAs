# HusTAs v0.1.0-preview.2

Second HusTAs Windows x64 preview / beta iteration.

This build focuses on turning the existing multi-agent group-chat experience into a bounded work environment without giving ordinary chats general access to the host filesystem.

## What's new

### Workspaces

Developers can create a workspace by selecting:

- a workspace name;
- an explicitly authorized local directory;
- participating human users;
- participating AI agents.

Each workspace creates its own group conversation using the same underlying group-chat implementation as ordinary groups.

Workspace group conversations retain normal collaboration features such as:

- group messages;
- mentions;
- replies / quotes;
- participant handling;
- shared-screen activity.

### Restricted file access

AI participants in a workspace receive a file-tree manifest for the authorized workspace directory and can read files inside that directory on demand.

Workspace access is intentionally bounded:

- ordinary chats do not receive workspace filesystem access;
- file requests are resolved relative to the selected workspace root;
- paths outside that root are rejected;
- cross-workspace access is rejected;
- workspace access does not add shell access, Python execution, Computer Use, or unrestricted host filesystem access.

### Permissions

Administrative capabilities are restricted to the Developer role.

Developer-only capabilities include:

- group creation and deletion;
- group membership management;
- workspace creation, deletion, and directory authorization;
- memory organization / management.

Ordinary users can:

- privately chat with AI agents;
- participate in group conversations they have been invited to;
- participate in workspace group conversations they have been invited to;
- view shared-screen activity available to that conversation.

Ordinary users do not receive group-management, workspace-management, or memory-management controls.

### Usage accounting and compatibility

- Workspace group usage is included in token accounting and is reported separately from ordinary group-chat usage.
- Imported personas can retain their configured provider ID even when that provider connection has not yet been configured; provider validation is deferred until the model is actually used.
- Existing conversation-access data receives compatibility handling without granting global access.
- Mention rendering resolves internal IDs to current display names.
- Mobile layout now keeps the current user's own messages aligned to the right.

## Before installing

- Treat this as preview / beta software and back up important local data.
- Download binaries only from the official HusTAs release surface.
- Windows may warn about an unsigned or low-reputation preview build until code signing and publisher reputation are established.
- Review `PRIVACY.md` before enabling external model, search, vision, workspace-file, or shared-screen features.
- Review `SECURITY.md` before granting a workspace access to local files.

The public repository does not include the private HusTAs implementation source.
