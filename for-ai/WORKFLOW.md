# Update workflow

1. Confirm the source PC app repository and this deployment repository are on their intended branches with no unrelated work.
2. Change companion source in the private PC app repository. Run its focused checks and `npm run build`.
3. Copy only `companion-dist/` contents here. Remove stale hashed assets after confirming the resolved target stays inside this deployment repository. Preserve `.nojekyll` and the control plane.
4. Run the asset and secret checks in [VERIFICATION.md](VERIFICATION.md). Keep passwords out of tool output, commits, URLs, and CI settings.
5. Stage explicit paths, review the diff, commit, and push without force. Verify the Pages build for the exact commit and open the HTTPS page.
6. Record any tested phone, browser, mouse, clipboard, and WebRTC route evidence in the owning source repository; update this control plane only for durable deployment facts.

Do not treat a successful Pages build as proof of a remote-control session.
