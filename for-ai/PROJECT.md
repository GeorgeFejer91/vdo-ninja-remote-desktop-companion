# Project contract

**Purpose:** Serve the personal remote desktop browser companion over HTTPS from GitHub Pages so a phone or browser can connect to the Windows PC app through VDO.Ninja-compatible WebRTC.

**Owner and source:** `GeorgeFejer91/vdo-ninja-remote-desktop-companion` is public and contains built static assets. The separate `GeorgeFejer91/vdo-ninja-remote-desktop` PC app repository is private and owns all editable companion, Tauri, and Rust source.

**Authority boundary:** The static page may collect a host password at runtime and initiate an encrypted browser-to-host session. It contains no password, desktop content, privileged proxy, or native command authority. The Rust PC app checks authorization before applying mouse or clipboard commands.

**Current verified state:** GitHub Pages serves <https://georgefejer91.github.io/vdo-ninja-remote-desktop-companion/> over HTTPS and renders the password form. A browser session from a different network and a physical phone have not yet been verified at this origin.

**Non-goals for this repository:** PC app binaries, Rust source, credentials, server-side Pages authentication, and a second implementation of the companion.
