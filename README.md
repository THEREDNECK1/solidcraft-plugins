
# SolidCraft Plugins Registry

The official community registry and distribution index for **SolidCraft** plugins and kernel extensions.

This repository hosts plugin manifests, package metadata, and automated builds for `index.json`, which powers the in-app **Community Plugin Browser** in SolidCraft.

---

## How It Works

1. **Manifest Repository**: Community developers submit plugin definitions via pull requests under the `plugins/` directory.
2. **Automated Indexing**: On every merge to `main`, a GitHub Actions workflow validates all manifests, extracts metadata, and compiles a unified `index.json` at the root.
3. **In-App Discovery**: SolidCraft queries the raw `index.json` endpoint to discover, filter, download, and hot-load WebAssembly (`.wasm`) features directly into the parametric modeling workspace.

---

## Submitting a Plugin

To publish a plugin to the registry:

### 1. Directory Structure
Create a dedicated subfolder in `plugins/` using reverse domain notation (`<vendor>.<plugin-name>`):

```text
plugins/
└── org.solidcraft.gear-generator/
    └── plugin.json
