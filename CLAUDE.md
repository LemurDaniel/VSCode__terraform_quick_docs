# Terraform Quick Docs (VS Code Extension)

Marketplace: `LemurDaniel.terraform-quick-docs` · Repo: LemurDaniel/VSCode__terraform_quick_docs

## Stack & Befehle
- JS (client = VS Code Extension, server = Language Server), webpack
- `npm install` (postinstall installiert client/server), `npm run lint`, `npm run package`
- Kein Testframework vorhanden

## Release
- Pipeline `.github/workflows/package.yaml`: Push auf master (client/server/package*.json) → vsce publish. Manuell: `workflow_dispatch` mit `skip_publish=false`. Version vor Merge bumpen, sonst schlägt Publish fehl. Bewusst keine GitHub Releases (Speicher)
- Version in package.json + package-lock.json + CHANGELOG (`## [<version>]`) pflegen
- Provider-Updates laufen automatisch (`providerCheck.yaml`)
- Security: `securityCheck.yaml` (So 03:00) → `npm audit fix --force` → PR auf Branch `automated_security_audit_fix`, kein Auto-Merge/Publish. Nach Review mergen → Push-Trigger veröffentlicht

## Konventionen
- Commits: Name `LemurDaniel`, Mail `landau.daniel.1998@gmail.com`
- Offene Sichtbarkeits-Themen: siehe HANDOVER.md

## Claude-Code-Tips
Die 16 Tips (https://raw.githubusercontent.com/aishwaryanr/awesome-generative-ai-guide/main/youtube/claude-code-16-tips.md) wurden am 2026-10-25 durchgegangen; Umsetzung: CLAUDE.md, HANDOVER.md, kaputtes `npm test` entfernt.
