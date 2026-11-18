# muk-mcp

Unmodified mirror of **MuK MCP Server** (`muk_mcp`) and its dependency **MuK Web Utils** (`muk_web_utils`)
for Odoo 18, by [MuK IT GmbH](https://www.mukit.at), as published on the
[Odoo App Store](https://apps.odoo.com/apps/modules/18.0/muk_mcp) under the [LGPL-3](muk_mcp/LICENSE).
Upstream does not publish these modules in a git repository; this one makes them installable from git.

Nothing here is changed by Qalisa: copyright notices, licenses and code are as downloaded. Qalisa's own
additions (OAuth 2.1 for MCP clients) live in a separate module, `muk_mcp_oauth`.

| Module | Version |
|---|---|
| `muk_mcp` | 18.0.3.2.11 |
| `muk_web_utils` | 18.0.1.0.4 |

## Use

Add this repository to Odoo's `addons_path`, branch `18.0`. At Qalisa it is cloned by
Qalisa/IaC (`nix/modules/odoo.nix`) for `odoo.qalisa.fr`.

## Syncing a new upstream release

One branch per Odoo version, one commit per imported release.

1. Download the new release from the App Store.
2. Replace `muk_mcp/` and `muk_web_utils/` with the archive's folders, update the versions above.
3. Commit as `Import MuK MCP Server <version> and MuK Web Utils <version>`, push.
4. Redeploy, then upgrade the module in Odoo (`-u muk_mcp`).
