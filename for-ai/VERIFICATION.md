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
