# STYXYBOT Updates

Official Android distribution downloads are published under Releases.

## Installation

Download the APK from the latest release and install it over the same STYXYBOT edition. Do not uninstall first: an in-place update preserves application data. Device activation is still required for the licensed edition.

The first version with the public updater must be installed manually. After that, use **Check for updates** in the app.

## Release publishing

Publish distribution APKs only. Never upload development APKs, signing keys, activation certificates, or private source code.

The updater reads the latest published GitHub release and matches an asset named:

`STYXYBOT-<Android application ID>-v<integer versionCode>.apk`

For the friend-licensed edition, the application ID is `com.styxy.bot.friendbeta`. Keep the existing signing certificate and increase the Android versionCode. GitHub must provide a `sha256:` digest for the uploaded asset. The app checks the downloaded hash, package name, signing certificate and version before handing installation to Android for user approval.

Keep the distribution release available through GitHub's latest-release endpoint. Describe beta limitations in its notes. A release without a matching APK is reported as unavailable for that edition.
