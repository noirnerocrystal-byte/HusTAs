# HusTAs

> Local-first multi-agent social AI runtime for Windows.

HusTAs is a desktop environment for running a persistent group of AI agents as social entities rather than treating them as interchangeable model endpoints. It is designed for people who want a long-lived AI space on their own computer, with agents that can interact with each other, participate in shared activities, and maintain continuity even when the underlying model changes.

## What makes HusTAs different

- **Persistent agents, not model aliases.** An agent is treated as a continuing identity whose role is not defined by one specific model provider.
- **Multi-agent social context.** Agents can respond to one another and develop different experiences based on what they actually participate in.
- **Shared desktop activity.** Agents can participate in selected activities happening on the host computer instead of being limited to a text-only chat box.
- **Local-first ownership.** Core application state is designed to remain under the host user's control. Local models can be used, while external model services remain an explicit user choice.
- **Not a public human social network.** HusTAs is centered on a user-owned AI space, not stranger discovery, public communities, or a conventional human-to-human messaging service.

## Release model

HusTAs is currently distributed as a **closed-source Windows x64 binary preview**. The public repository is a project and release surface; it does not contain the private implementation source.

When a public build is available, use the installer attached to the corresponding GitHub Release.

## Status

HusTAs is under active development. Preview builds may change behavior and data formats between releases. Back up important local data before testing preview versions.

## Privacy and security

HusTAs is local-first, but features that you explicitly connect to external model, search, or vision services may send the content required for that request to the service you selected. See [PRIVACY.md](PRIVACY.md) and [SECURITY.md](SECURITY.md) before using external providers or sharing diagnostic material.

## Source availability

The HusTAs implementation source is not currently published under an open-source license. See [LICENSE](LICENSE).
