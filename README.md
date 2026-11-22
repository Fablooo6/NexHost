# NexHost

NexHost is a Windows desktop application for managing local Minecraft Java
Edition servers, with an integrated client launcher currently in development.

The application is built with Python, `pywebview` and a plain HTML/CSS/JS
frontend. It runs entirely on the user's PC and stores its data next to the
application in a portable `data/` folder.

## Features

- Create and manage Minecraft Java Edition servers (Vanilla, Fabric, Forge)
- Start, stop and monitor servers, including a live console
- Install and update server mods and modpacks from CurseForge
- Download and manage isolated Java runtimes on demand
- Optional multiplayer helpers (e4mc, playit.gg, Tailscale)
- Optional local AI assistant and Discord notifications
- Integrated Minecraft Java Edition launcher (in development)

## Minecraft launcher and Microsoft accounts

The integrated launcher is designed around genuine Microsoft accounts only:

- Sign-in uses the Microsoft OAuth 2.0 device code flow with NexHost's own
  public Azure client. No client secret is shipped.
- Refresh tokens are encrypted at rest with Windows DPAPI. Access tokens are
  kept in memory only and are never written to logs.
- Before a game launch is enabled, NexHost verifies game ownership through the
  official Minecraft profile endpoint.
- Offline, cracked or alternative account systems are not supported.
- NexHost does not distribute Minecraft game files. Game files, assets and
  libraries are downloaded from the official Mojang services.

NexHost is currently awaiting Microsoft approval for Minecraft API access for
its Azure application. Until that approval is granted, the Minecraft sign-in
cannot complete.

## Privacy

See [PRIVACY.md](PRIVACY.md) for details about data handling, network requests
and local storage.

## Status

NexHost is an independent project in active development. Server management is
available; the integrated client launcher is being completed.

## Contact

Please use the GitHub issue tracker of this repository for questions and
security reports.
