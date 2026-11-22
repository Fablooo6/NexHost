# Privacy

NexHost is a local Windows desktop application. It does not operate any
NexHost backend, telemetry service or analytics service.

## Data stored locally

NexHost stores its data in a portable `data/` folder next to the application:

- Application settings and instance metadata (JSON)
- Server files, logs and backups created by the user
- Downloaded Java runtimes and Minecraft assets/libraries
- Microsoft account metadata (account name, UUID, skin URL)
- Microsoft refresh tokens, encrypted with Windows DPAPI

Access tokens are kept in memory only. Passwords are never stored. Microsoft
sign-in uses the OAuth 2.0 device code flow, so the Microsoft password is only
entered on Microsoft's own website.

## Network requests

NexHost only contacts remote services that are required for the features the
user actively uses:

- Microsoft, Xbox Live and Minecraft services for account sign-in, token
  refresh and game ownership verification
- Mojang services for version metadata, assets, libraries and Java runtimes
- CurseForge for mod and modpack catalogs (if the feature is used)
- Optional third-party services configured by the user, such as AI providers
  or multiplayer tunnel providers

NexHost does not upload game files, account tokens or server data to its own
servers. There are no NexHost servers.

## Logs

Logs are stored locally. Authentication tokens are not written to logs.
Server console output may be stored locally as part of normal server
management.

## Contact

Please use the GitHub issue tracker of this repository for privacy questions.
