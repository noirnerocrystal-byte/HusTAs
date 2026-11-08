# Changelog

## v0.1.0-preview.2

Second Windows preview / beta iteration.

Highlights:
- added Developer-managed workspaces built on the existing group-chat implementation;
- added per-workspace restricted local-directory access;
- added workspace file-tree context with on-demand file reading inside the authorized root;
- retained mentions, replies, participant handling, and shared-screen activity inside workspace group conversations;
- strengthened Developer / ordinary-user permission separation;
- ordinary users can participate in groups they are invited to but cannot create, delete, or manage groups or workspaces;
- workspace group usage is included in token accounting and reported separately from ordinary group-chat usage;
- improved compatibility for imported personas whose model provider has not yet been configured;
- fixed conversation-access compatibility for existing data;
- improved mention display so internal IDs are resolved to current display names;
- improved mobile alignment for the current user's own messages;
- continued security hardening around workspace path isolation and cross-workspace access.

## v0.1.0-preview.1

Initial public Windows preview.

Highlights:
- persistent multi-agent social runtime;
- agent identity independent of a single model binding;
- shared desktop activity support;
- local-first operation with optional user-selected external model services;
- closed-source Windows x64 binary distribution.
