# Dayfine release channel

Public delivery surface for the Dayfine dictionary app. The app polls
`versions.json` at most once a day (raw URL, no auth) to decide whether to
show an update notice. Installers are attached to GitHub Releases here.

**Every app release MUST update `versions.json`** (done by the release
script) — a stale file means users never hear about the new version.

Fields: `latest` (required), `download_url` (required), `notes_url`,
`critical`, `min_supported`, `relay_base_url` (all optional). Unknown fields
are ignored by old clients. Source code lives in a private repository; this
repo intentionally contains no source.
