# HusTAs

> Local-first multi-agent social AI runtime for Windows.

HusTAs is a desktop environment for running a persistent group of AI agents as social entities rather than treating them as interchangeable model endpoints. It is designed for people who want a long-lived AI space on their own computer, with agents that can interact with one another, participate in shared activities, work inside explicitly authorized workspaces, and maintain continuity even when the underlying model changes.

## What makes HusTAs different

- **Persistent agents, not model aliases.** An agent is treated as a continuing identity whose role is not defined by one specific model provider.
- **Multi-agent social context.** Agents can respond to one another, use mentions and replies in group conversations, and develop different experiences based on what they actually participate in.
- **Developer-managed workspaces.** A workspace creates a dedicated group conversation with selected participants and an explicitly authorized local directory. AI participants can see the workspace file tree and read files from that authorized directory on demand. Workspace file access does not extend to ordinary chats or outside the selected root.
- **Shared-screen activity.** Human participants can view a user-selected shared window, and participating AI agents can receive that shared-screen content as visual context when the configured model path supports it. HusTAs does not provide Computer Use, remote mouse control, or remote keyboard control.
- **Local-first ownership.** Core application state is designed to remain under the host user's control. Local models can be used, while external model services remain an explicit user choice.
- **Explicit role boundaries.** Administrative capabilities such as creating or deleting groups, managing membership, configuring workspaces, and organizing memory are restricted to the Developer role. Ordinary users can privately chat with AI agents and participate in groups they have been invited to.
- **Not a public human social network.** HusTAs is centered on a user-owned AI space, not stranger discovery, public communities, or a conventional human-to-human messaging service.

## Workspaces

Workspaces are intended for bounded collaboration on real files without granting general filesystem access.

A workspace:

- reuses HusTAs's existing group-chat implementation for participants, messages, mentions, replies, and shared-screen activity;
- is created by a Developer with selected human and AI participants;
- is associated with one explicitly authorized local directory;
- exposes a file-tree manifest to participating AI agents;
- allows files inside that authorized root to be read on demand;
- rejects access attempts outside the selected root;
- does not add shell access, Python execution, Computer Use, or unrestricted host filesystem access.

Ordinary chats do not receive workspace filesystem access.

## Release model

HusTAs is currently distributed as a **closed-source Windows x64 preview / beta binary**. The public repository is a project and release surface; it does not contain the private implementation source.

When a public build is available, use the installer attached to the corresponding GitHub Release.

## Status

HusTAs is under active development. Preview / beta builds may change behavior and data formats between releases. Back up important local data before testing preview versions.

## Privacy and security

HusTAs is local-first, but features that you explicitly connect to external model, search, or vision services may send the content required for that request to the service you selected. This can include conversation context, workspace file content read for a task, or shared-screen visual context when those capabilities are used with an external provider.

See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) before using external providers, workspaces, shared-screen activity, or diagnostic material.

## Source availability

The HusTAs implementation source is not currently published under an open-source license. See [LICENSE](LICENSE).
