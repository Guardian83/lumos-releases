# Lumos — approved downloads

This repository contains approved Lumos app downloads and update information only. Application source code is kept in a separate private repository.

A permanently signed [Android preview build 1019](https://github.com/Guardian83/lumos-releases/releases/tag/android-preview-1019) is available for manual download. Its backend is not configured, so backend login and remote device features are unavailable on physical phones.

No production update has been approved yet. This preview has no `update.json` and is excluded from the automatic update feed.


## Android preview

[Download the signed Android APK](https://github.com/Guardian83/lumos-releases/releases/download/android-preview-1019/lumos-android-build-1019.apk). The preview includes checksums, public signing-certificate information and source-build provenance. No private key or signing password is published.

This APK establishes the permanent signing identity used for future Android releases. An existing installation signed with a different/debug key cannot be updated in place by this APK. Preserve/export data before any manual migration; do not remove an installed app simply to force an update.

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
