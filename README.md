# GitHub Runner — update feed

This repository exists so the [GitHub Runner](https://github.com/SaschaHenning/mac-runner)
menu-bar app can update itself. The app's source stays private; only the built,
signed and notarized application is published here, because Sparkle needs a feed
and an archive it can fetch without credentials.

- `appcast.xml` — the feed the app reads.
- Releases — one per version, each with the app as a ZIP.

Every archive is signed twice: with Sascha Henning's Apple Developer ID (so macOS
accepts it) and with the project's EdDSA key (so Sparkle accepts it). An archive
that fails either check is refused by the app before it replaces anything.

Nothing here is meant to be edited by hand. The release workflow in the private
repository publishes it.
