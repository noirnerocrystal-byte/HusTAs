# Privacy

HusTAs follows a **local-first** model: the host user controls the application instance and its local state.

## Local operation

Core conversations, agent configuration, relationships, memories, workspace configuration, and other runtime state are designed to be stored on the host computer rather than in a HusTAs-operated central service.

Protect that local data as you would other private application data.

## External services

HusTAs can optionally use services selected and configured by the user, such as external language models, search providers, or vision-capable models.

When such a feature is enabled, the content required to perform that request may be sent to the selected third-party service. Depending on the feature and model configuration, that content may include:

- conversation messages and relevant conversation context;
- agent or memory context required for a response;
- workspace file-tree metadata;
- content from a workspace file read for the current task;
- shared-screen visual context when an AI participant is given that visual input.

The third party's own terms, privacy practices, retention policies, and account settings then apply.

Using a fully local model path can keep more processing on the host. Using an external provider necessarily changes that boundary. HusTAs should therefore not be interpreted as claiming that data "never leaves the device" under every configuration.

## Workspaces and local files

A workspace can be associated with one local directory explicitly selected by the Developer.

Workspace file access is intended to remain scoped to that authorized root. Ordinary chats do not receive workspace filesystem access merely because workspace functionality exists elsewhere in the application.

If an externally hosted model is used inside a workspace, workspace metadata and file content read for that conversation may be sent to the selected model provider as part of the request.

Grant workspace access only to directories whose contents you are comfortable using with the configured models and participants.

## Shared-screen activity

Shared-screen activity is initiated explicitly by a human user.

Screen content may be visible to human participants in the conversation and, when configured, may be provided as visual context to participating AI models.

HusTAs shared-screen activity does not by itself provide Computer Use, remote mouse control, or remote keyboard control.

## Human participants

If other people are invited into a HusTAs instance, their messages and activity become part of the host-controlled instance. The host user is responsible for using and sharing that data appropriately.

Workspace group participants may see conversation content and shared-screen activity available to that conversation. They may also see AI responses that quote, summarize, or otherwise use content read from files inside the workspace's authorized directory. Workspace management and filesystem authorization remain restricted to the Developer role.

## Diagnostics and backups

Logs, backups, exported data, screenshots, or diagnostic bundles may contain sensitive information, including conversation text, local paths, workspace metadata, model configuration, or provider information.

Review diagnostic material before sharing it and do not publish credentials, private conversation data, or sensitive local-file contents.
