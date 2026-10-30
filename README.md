# Lumos — approved downloads

This repository contains approved Lumos app downloads and update information only. Application source code is kept in a separate private repository.

No app version has been approved for public release yet. Files will appear under [Releases](https://github.com/Guardian83/lumos-releases/releases) after the owner tests and approves a build.

## iPhone installation with iLoader

1. Download `smart_home_unsigned.ipa` from an approved release to your computer.
2. Connect your iPhone and open [iLoader](https://github.com/nab138/iloader).
3. Sign in with the same Apple ID and use the same app identity/options used for your existing Lumos installation.
4. Install the new IPA over the existing app. Do not delete the old app to update it; Lumos data is stored locally.

The IPA is unsigned. iLoader handles signing and installation. Lumos can notify you about an approved version, but cannot silently replace an iLoader-installed iPhone app.

The first version with update checking must be installed manually. After that, the app checks this repository for approved releases.

## Release policy

- New source-code pushes build private test candidates only.
- The owner must approve a specific successful build before publication.
- Approval publishes the tested binaries, without rebuilding them.
- iPhone-only releases do not include an Android APK.
- Each release includes `update.json` and `SHA256SUMS`.

Update feed (available after the first approved release):
`https://github.com/Guardian83/lumos-releases/releases/latest/download/update.json`

Lumos is currently a development preview; device controls are simulated.
