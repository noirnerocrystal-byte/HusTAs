# Privacy

HusTAs follows a **local-first** model: the host user controls the application instance and its local state.

## Local operation

Core conversations, agent configuration, relationships, memories, and other runtime state are designed to be stored on the host computer rather than in a HusTAs-operated central service. Protect that local data as you would other private application data.

## External services

HusTAs can optionally use services selected and configured by the user, such as external language models, search providers, or vision-capable models. When such a feature is enabled, the content required to perform that request may be sent to the selected third-party service. The third party's own terms and privacy practices then apply.

Using a fully local model path can keep more processing on the host; using an external provider necessarily changes that boundary. HusTAs should therefore not be interpreted as claiming that data "never leaves the device" under every configuration.

## Human participants

If other people are invited into a HusTAs instance, their messages and activity become part of the host-controlled instance. The host user is responsible for using and sharing that data appropriately.

## Diagnostics and backups

Logs, backups, exported data, screenshots, or diagnostic bundles may contain sensitive information. Review them before sharing and do not post credentials or private conversation data publicly.
