## Fork note

This fork exists **only** to add a native Android Picture-in-Picture path to
the main video player. Upstream's "popup" mode is a `SYSTEM_ALERT_WINDOW`
overlay, which Android marks as obscuring the underlying app — apps that opt
into tap-jacking protection (Gmail's account switcher, GitHub's OAuth
webviews, etc.) then silently drop taps until the popup is closed. Native
PiP is system-managed and doesn't trigger that filter.

`upstream/dev` is merged into `dev` daily via
`.github/workflows/sync-upstream.yml`; if the merge conflicts, the workflow
fails visibly and it needs to be resolved by hand. If you want the classic
upstream behavior, use upstream's build — nothing else is intentionally
different here.

## README

The client of [PipePipe](https://codeberg.org/NullPointerException/PipePipe).
