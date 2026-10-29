# Changelog — role-release-captain

## 0.1.1 — 2026-10-28

The repo is public. The role is unchanged: `role.json` and `prompt.md` are byte for byte as in 0.1.0.

- README: any computer can fetch the repo, so galt needs no vault token. galt's scheduler supports publishing the role from this Element (`role_elements`).
- CLAUDE.md rule 7: the repo is public, so no secrets, credentials, customer data or production data go in it.
- `bin/check-role` check 8: fails on secret-shaped strings (GitHub, OpenAI, Google, Slack and AWS tokens, private keys). The canonical validator is now check 9.

## 0.1.0 — 2026-10-28

First release, as a role module. Role `release-captain` version 7, from vsi-tenant `roles/release-captain.md` at `fd0c872`. `prompt.md` is that file's body byte for byte, and `role.json` is its front matter.

- `rasa.json`: `kind: module`, named `rasa.module.role.release-captain`, with no permissions.
- `.claude-plugin/plugin.json`, so a session or agent can load it (galt ADR 0064).
- `bin/check-role`: the release gate.
