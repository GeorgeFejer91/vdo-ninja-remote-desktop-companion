# Verification gates

Use `VERIFIED`, `PARTIAL`, `BLOCKED`, or `NOT RUN`; name the surface actually observed.

## Bootstrap

Run `pwsh -NoProfile -File for-ai/scripts/check-context.ps1 -ProjectRoot . -RequireRemote` after publishing. It must pass with a clean tree and local `HEAD` equal to `origin/main`.

## Focused asset check

Build the private PC app repository with `npm run build`. Copy only the generated `companion-dist/` files to this repository root. Verify `index.html` references assets that exist here. Compare the deployed text assets against the host's generated password without printing that password. Confirm no host files, credentials, logs, or `.env` files were copied.

## Integrated check

GitHub Pages must report the new commit as built and return HTTP 200 over HTTPS with the password form and its assets. When a live host is available, authenticate from the deployed origin, observe desktop video, and exercise the mouse and clipboard paths. A same-machine browser test does not qualify a phone or a WAN/TURN route.

## Publication

Review status and diff, stage intended paths only, commit, push without force, and verify `origin/main`, Pages build status, and the public page. Keep the PC app source repository private unless the user explicitly changes that decision.

## 2026-10-02 baseline

- `VERIFIED`: The public GitHub Pages repository deployed static assets from the private source build, and the HTTPS page returned HTTP 200 with its password form.
- `VERIFIED`: The generated host password was absent from the static text assets at publication.
- `NOT RUN`: Live authenticated session from the GitHub Pages origin, physical phone, WAN/TURN route, and performance measurement.

## 2026-10-02 phone navigation bundle

- `VERIFIED`: The new static bundle was copied byte-for-byte from private PC app source commit `e8fceb0ec668597a2e415da49524218ddd86d3e1` after `npm run build`. Its HTML references the included hashed CSS and JS assets.
- `VERIFIED`: A local preview of this browser UI authenticated to the existing Windows host and displayed live desktop video. The Display and Clipboard panels opened, zoom changed to 125%, and the mode control switched between mouse and touch.
- `VERIFIED`: The generated host password is absent from the public repository text assets. GitHub Pages served the preceding phone-control bundle over HTTPS and returned HTTP 200 for its HTML, CSS, and JS.
- `NOT RUN`: Authentication from this exact deployed bundle, physical phone gestures, WAN/TURN route, and performance measurement. The host is currently stopped until its password is replaced locally.
