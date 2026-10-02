# VDO.Ninja Remote Desktop companion

Open the [browser companion](https://georgefejer91.github.io/vdo-ninja-remote-desktop-companion/) from a phone or desktop browser. The Windows PC app has a [separate private repository](https://github.com/GeorgeFejer91/vdo-ninja-remote-desktop).

This public repository contains only static assets deployed through GitHub Pages. Desktop video, mouse control, and clipboard access require the password displayed by the Windows host application. GitHub Pages itself serves this page publicly; no host password is stored here.

The companion provides mouse and touch navigation, clicks and dragging, right click, scrolling, zoom and pan, and two-way text clipboard controls. The Windows host currently captures its primary display. Keyboard control, file transfer, and the full RustDesk settings catalog are not implemented.

To update the companion, build the PC app repository with `npm run build`, review `companion-dist/` for secrets, copy those files to this repository root, remove obsolete hashed assets, and verify the Pages deployment. See [for-ai/README.md](for-ai/README.md) for the repository workflow.
