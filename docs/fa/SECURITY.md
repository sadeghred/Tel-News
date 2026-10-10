# امنیت

Repository عمومی فقط برای مستندات است و نباید Secretهای Production را افشا کند.

موارد ممنوع برای انتشار:

- Telegram API Credential یا Bot Token
- API Keyهای AI Provider
- Secretهای داخلی AI-Hub
- Password
- آدرس خصوصی Server یا SSH Credential
- Database Production یا Credential آن
- Session file
- Credential کانال/Account خصوصی
- Log و Backup خام Production
- آرشیو سورس خصوصی قابل Deploy

Credentialهای Source و Output Adapter باید خارج از مستندات عمومی و Exampleهای سورس نگهداری شوند.
