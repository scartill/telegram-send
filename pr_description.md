## Summary

This Pull Request introduces the ability to send messages to specific chat IDs or predefined aliases without modifying the configuration file. It also adds support for securely configuring the bot token via an environment variable.

## Changes

- **New CLI Arguments:**
  - `--chat-id <ID>`: Sends a message directly to the specified chat ID, overriding the configured one.
  - `--alias <ALIAS>`: Sends a message to a predefined alias mapping (stored in the `[aliases]` block in the configuration file).

- **Environment Variable for Bot Token:**
  - Added support for the `TELEGRAM_BOT_TOKEN` environment variable.
  - Using `--configure` with this variable set bypasses the interactive prompt, allowing for secure token usage without storing it in a plain-text configuration file.

- **Documentation Updates:**
  - Updated `README.md` to document the new `--chat-id` and `--alias` features, along with an example `[aliases]` block configuration.
  - Updated `README.md` to document the new `TELEGRAM_BOT_TOKEN` environment variable behavior.
