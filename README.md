# Lumos — app downloads

This repository contains signed test previews, approved app downloads and update information. Application source code is kept in a separate private repository.

The signed [Android local test preview build 1022](https://github.com/Guardian83/lumos-releases/releases/tag/android-preview-1022) is available for manual download. It works without a backend or SMS service: enter a valid Iranian phone number and use test code **12345** to open a sample home with simulated devices.

No production update has been approved yet. Local test previews have no `update.json` and are excluded from the production update feed.


## Android preview

Signup fixes: fixed phone/OTP labels, a clear white back arrow, keyboard-safe navigation, and an explicitly labeled offline test login. No SMS is sent; use **12345**. Test accounts/settings are isolated from real backend data.

[Download the signed Android APK](https://github.com/Guardian83/lumos-releases/releases/download/android-preview-1022/lumos-android-build-1022.apk). The preview includes checksums, public signing-certificate information and source-build provenance. No private key or signing password is published.

Build 1022 uses the same permanent signing key as signed preview 1019, so it can be installed over that preview without uninstalling. An existing installation signed with a different/debug key cannot be updated in place by this APK. Preserve/export data before any manual migration; do not remove an installed app simply to force an update.

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
- Each production release includes `update.json` and `SHA256SUMS`. Manual previews include checksums but do not change the update feed.

Update feed (available after the first approved release):
`https://github.com/Guardian83/lumos-releases/releases/latest/download/update.json`

Lumos is currently a development preview; device controls are simulated.
