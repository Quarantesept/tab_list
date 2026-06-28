# Technical Documentation — OpenList Chrome Extension

Updated: 2026-06-28

## Purpose

OpenList Chrome Extension is maintained as a **Chrome extension utility**. This file is the technical entrypoint for implementation, operations and verification details that should not be buried in chat history.

## Architecture

- **Primary stack**: Chrome extension manifest + vanilla JavaScript + static popup/background pages
- **Runtime/service**: ``chrome://extensions` developer mode or Chrome Web Store package`
- **Top-level layout**: `.gitignore`, `CHANGELOG.md`, `chrome_store/`, `docs/`, `extension/`, `icon.png`, `icon.pxm`, `LICENSE`, `README.md`

## Manifests And Dependencies

- No package manifest detected; inspect the project-specific runtime files.

## Runtime

```bash
# Load `extension/` as an unpacked Chrome extension
# or package the `extension/` folder for distribution.
```

## Verification

Run the lightweight checks before claiming a documentation or behavior change is complete:

```bash
node --check extension/background.js
node --check extension/openlist-lib.js
node --check extension/openlist-popup.js
```

For UI, game, WebGL, mobile or browser-heavy projects, add a visual/browser check when the change affects runtime behavior. Documentation-only changes can stop at README/CHANGELOG/doc consistency checks.

## Configuration And Secrets

- Do not commit `.env`, credentials, local database dumps, generated outputs or machine-specific runtime state.
- Keep example config files versioned (`.env.example`, `config.example.php`, sample JSON) when the project needs them.
- If a service name, port, domain or deployment path is documented, verify it with the actual service/tooling before presenting it as current.

## Documentation Maintenance

- `README.md` is the operational overview and quick-start.
- `CHANGELOG.md` records every documentation sweep and user-visible change.
- `docs/TECHNICAL_DOCUMENTATION.md` is the durable technical reference.
- `ROADMAP.md` remains the planning surface when present.
- Shared documentation principles live in `loomia-ops/docs/GITHUB_PROJECT_DOCUMENTATION_PRINCIPLES.md`.

## Maintainer Notes

- Public browser utility for opening URL/search-term lists in tabs.
- Preserve the no-build static extension model unless a migration is intentional.
