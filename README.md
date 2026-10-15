# C-OS-UPDATE

The update source of C-OS. GitHub Pages serves this repository; C-OS looks at
`https://kawanakatomoya374-pixel.github.io/C-OS-UPDATE/updates/manifest.cosup`.

- `updates/manifest.cosup` - the signed list of what is current (text; the signature follows the `--SIG--` line)
- `updates/*.bin` - the programs, each named in the manifest with its SHA-256

Nothing here is trusted just because it is here: C-OS accepts a manifest only if it is signed with the release key whose public half is
`release/update_public.pem` in the C-OS source repository, and every file only if its SHA-256 is the one in the manifest.

Do not edit by hand. Releases are made with `tools/release_update.py` and `tools/publish_pages.sh` of the C-OS source repository, which replace this repository's content with one
commit (so the history does not grow with every release).

Pages: Settings > Pages > Deploy from a branch > `main` / (root).
