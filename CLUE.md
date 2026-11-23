# Clue

Clue is a personal coding agent derived from OpenAI Codex under the Apache
License 2.0. This fork keeps upstream history, license and notices. Its
starting point is [Codex 0.171.0](https://github.com/openai/codex/releases/tag/rust-v0.171.0).
Changes in this fork include a separate CLI and profile, plus model selection
for a locally configured OpenAI-compatible Responses gateway.

The EL8 artifact preserves the upstream runtime layout. Extract it into its
own directory and add that directory's `bin` to PATH. Start the interactive
CLI with `clue` or the JSON-RPC server with `clue app-server`.

Clue stores config, logs and threads under `~/.clue` by default. An existing
directory set via `CLUE_HOME` overrides the default. Existing Codex profiles
remain under their own location. For a custom model, configure `model`,
`model_provider` and a provider that implements `wire_api = "responses"`.
