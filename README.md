# OpenList Chrome Extension

<!-- README_SYNC:START -->

## Documentation Status (2026-06-28)

- **Project type**: Chrome extension utility
- **Primary stack**: Chrome extension manifest + vanilla JavaScript + static popup/background pages
- **Runtime/service**: `chrome://extensions` developer mode or Chrome Web Store package
- **Canonical docs**: this `README.md`, `CHANGELOG.md`, `docs/TECHNICAL_DOCUMENTATION.md`, and project-specific files in `docs/` or `ROADMAP.md` when present.
- **Global documentation principles**: see `loomia-ops/docs/GITHUB_PROJECT_DOCUMENTATION_PRINCIPLES.md`.

### Quick Commands

Run:
```bash
# Load `extension/` as an unpacked Chrome extension
# or package the `extension/` folder for distribution.
```

Verify:
```bash
node --check extension/background.js
node --check extension/openlist-lib.js
node --check extension/openlist-popup.js
```

### Maintainer Notes
- Public browser utility for opening URL/search-term lists in tabs.
- Preserve the no-build static extension model unless a migration is intentional.

<!-- README_SYNC:END -->

OpenList helps you manage lists of URLs. It's useful if you have a habit of emailing yourself lists of articles or pages to check out later.

With OpenList, you can:

* select a list of URLs (or search terms) in any web page or textarea, then open them all in new tabs
* paste a list of URLs (or search terms) into a popup, then open them all in new tabs
* get a list of all tabs in the current window

The name should probably be changed to something like TabsList, but that's a lot of effort.

## Installation

[Download the extension from the Chrome store](https://chrome.google.com/webstore/detail/nkpjembldfckmdchbdiclhfedcngbgnl). It's free!

## Issues

Please open an issue on [the GitHub issue tracker for this project](https://github.com/cdzombak/OpenList/issues).

## History

* v0.3.3: remove redundant addition of context menu item
* v0.3.2: use Chrome event page instead of persistent background page, for reduced resource usage
* v0.3.1: fix a bug where Open button sometimes didn't work; appearance updates.
* v0.3: compatibility and security improvements; new icon.
* v0.2.2 removes warning when opening many tabs; this caused problems in some cases, and Chrome handles it decently well.
* v0.2 adds list generation capability & popup to enter a list from elsewhere; improves URL detection
* v0.1 initial release

## License

MIT. See `LICENSE` included in this repo.

## Developer

* [chris.dzombak.name](http://chris.dzombak.name/)
* chris@chrisdzombak.net
* [t@cdzombak](https://twitter.com/cdzombak)
* [a@dzombak](https://alpha.app.net/dzombak)
