# App releases

Signed Android builds and the update feeds that installed apps read. Nothing secret is stored here.

- `<app>/latest.json` is the feed. It holds the newest `versionCode`, `versionName`, the APK `url`, its `sha256` and `size`, and a `format` number. Apps ignore a format they don't know.
- Each build is a release tagged `<app>-<versionCode>` with the APK attached.
- A new app adds a folder and a release tag prefix. Nothing else changes.

Apps install an update only if its size and SHA-256 match the feed and Android confirms it is signed with the same key as the installed app.
