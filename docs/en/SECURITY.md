# Security

The public repository is documentation-only and must not expose production secrets.

Do not publish:

- Telegram API credentials or bot tokens
- AI-provider API keys
- AI-Hub internal authentication secrets
- passwords
- private server addresses or SSH credentials
- production database files or credentials
- session files
- private channel/account credentials
- raw production logs or backups
- deployable private source archives

Source and output adapters should keep platform credentials outside public documentation and source examples.
