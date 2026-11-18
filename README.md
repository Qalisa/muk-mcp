# muk-mcp (Qalisa fork)

Qalisa's copy of **MuK MCP Server** (`muk_mcp`) and its dependency **MuK Web Utils** (`muk_web_utils`) for
Odoo 18, by [MuK IT GmbH](https://www.mukit.at), distributed under the
[LGPL-3](muk_mcp/LICENSE) from the [Odoo App Store](https://apps.odoo.com/apps/modules/18.0/muk_mcp).
The upstream modules are not published in a git repository, hence this one.

## Branches

- `upstream`: the modules exactly as downloaded, one commit per App Store release.
- `18.0`: what runs at Qalisa (`odoo.qalisa.fr`), i.e. `upstream` plus our changes, listed below.
  Deployed by Qalisa/IaC (`nix/modules/odoo.nix`), which clones this branch.

## Qalisa changes

None yet.

## Updating from upstream

1. Download the new release from the App Store.
2. `git checkout upstream`, replace `muk_mcp/` and `muk_web_utils/`, commit "Import MuK MCP Server <version>".
3. `git checkout 18.0 && git merge upstream`, resolve, push.
4. Redeploy bud and upgrade the module in Odoo (`-u muk_mcp`).

Copyright notices and the LGPL-3 license of the upstream code are kept unchanged.
