# Lumos — Android and iPhone downloads

Current owner-approved offline test update: **build 1034**. This version removes the test-version title from the authentication footer and top banner.

- [Download the signed Android APK](https://github.com/Guardian83/lumos-releases/releases/download/mobile-preview-1034/lumos-android-build-1034.apk)
- [Download the unsigned iPhone IPA for iLoader](https://github.com/Guardian83/lumos-releases/releases/download/mobile-preview-1034/lumos-iphone-build-1034-unsigned.ipa)
- [Release notes and checksums](https://github.com/Guardian83/lumos-releases/releases/tag/mobile-preview-1034)

## Update an installed app

Restart Lumos with internet connected to receive the update prompt. The active update feed now includes both platforms.

**Android:** current versions download inside Lumos with percentage progress, cancellation and retry. Android asks you to confirm installation. The permanent signing key is the same as builds 1019, 1022 and 1027. Install over the existing signed app; do not uninstall it. Builds signed with a different/debug key require a separate migration.

**iPhone:** download the IPA to your computer and import it in [iLoader](https://github.com/nab138/iloader). iLoader handles signing with your Apple ID. Use the same Apple ID and app identity/settings as your existing Lumos installation, and install over it. The IPA is unsigned; the app cannot silently replace an iLoader-installed iPhone app. Bundle identity: `ir.minisaeb.smartHome`; minimum iOS: 15.0.

## Offline test login

Enter a valid Iranian phone number, such as **09120000000**, and use code **12345**. No backend or SMS is needed. A sample home with five simulated devices opens. Test data is local and isolated from real backend data; device controls are simulated.

## Release policy

Source code is kept in a separate private repository. Source pushes build private candidates. The owner approves a particular tested build for publication; the exact tested binaries are published without rebuilding. This preview was explicitly approved for both Android and iPhone update delivery.

Each update includes `update.json`, `SHA256SUMS` and build provenance. Android releases include the public signing certificate. Private keys and signing passwords are never published.

Active update feed: `https://github.com/Guardian83/lumos-releases/releases/latest/download/update.json`.
