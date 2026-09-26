# legotypes.github.io

The LegoTypes project pages, served by GitHub Pages at <https://legotypes.github.io/>
from the root of `main`. Plain static HTML with one shared stylesheet: no build step,
no Jekyll (`.nojekyll`), no external scripts or fonts.

## Pages

| Path | Page |
|---|---|
| `/` | Landing: the plugins as a card grid, and the install one-liner |
| `/install/` | Adding the signed LegoTypes package repository to OPNsense: the bootstrap command, the signing-key fingerprint and how to check it, updates and removal |
| `/wg-upstream-tunnels/` | `os-wg-client-tunnels`: why, what it builds and enforces, settings, findings, command line |
| `/avahi-reflector/` | `os-avahi-reflector`: mDNS/DNS-SD reflection across VLANs |
| `/mac-alias-cache/` | `os-mac-alias-cache`: MAC alias inspection and rebuild |
| `/assets/site.css` | The stylesheet: light and dark via `prefers-color-scheme`; a page with a contents sidebar uses `<div class="page with-toc">` |

Each plugin's `PLUGIN_WWW` points at its page, so the paths above are part of the
packages; renaming one needs a plugin release.

The package repository itself is not here: it is published by
[`LegoTypes/opnsense-repo`](https://github.com/LegoTypes/opnsense-repo) under
<https://legotypes.github.io/opnsense-repo/>.

## Editing

Edit the HTML, open it in a browser to check (it renders the same from disk), then
push to `main`; Pages deploys within a minute or two. `main` is protected by a
ruleset (no deletion, no force-push; organization and repository admins bypass).

Keep examples on the pages to documentation address ranges (192.0.2.0/24,
198.51.100.0/24, 203.0.113.0/24, 2001:db8::/32) and synthetic names.

If the repository's signing key changes, update the fingerprint on `/install/` in
the same change that publishes the new key.
