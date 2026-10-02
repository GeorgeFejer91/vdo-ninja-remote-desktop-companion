# Decisions

## D1 — Separate public GitHub Pages repository

**Status:** Accepted, 2026-10-02.

**Decision:** Keep the PC app and editable companion source in the private `GeorgeFejer91/vdo-ninja-remote-desktop` repository. Publish only generated browser assets from this public repository with GitHub Pages.

**Reason:** The current GitHub account plan rejected Pages from the private repository. The user chose GitHub Pages and authorized a public companion. Static Pages content is public, while the Windows host requires its generated password before video, mouse, or clipboard access.

**Consequence:** A deployment copies a reviewed source build into this repository. There is no server-side password gate on the static page. Do not add passwords, desktop data, or PC app source here.
