# Terraform Quick Docs (VS Code Extension)

Marketplace: `LemurDaniel.terraform-quick-docs` · Repo: LemurDaniel/VSCode__terraform_quick_docs

## Stack & Befehle
- JS (client = VS Code Extension, server = Language Server), webpack
- `npm install` (postinstall installiert client/server), `npm run lint`, `npm run package`
- Kein Testframework vorhanden

## Release
- Pipeline `.github/workflows/package.yaml` (`workflow_dispatch`, `skip_publish=false` auf master): vsce package → publish. Bewusst keine GitHub Releases (Speicher)
- Version in package.json + package-lock.json + CHANGELOG (`## [<version>]`) pflegen
- Provider-Updates laufen automatisch (`providerCheck.yaml`)
- Security: `securityCheck.yaml` (So 03:00) → `npm audit fix --force` → PR auf Branch `security_audit_fix`, kein Auto-Merge/Publish. Nach Review mergen und `package.yaml` manuell starten

## Konventionen
- Commits: Name `LemurDaniel`, Mail `landau.daniel.1998@gmail.com`
- Offene Sichtbarkeits-Themen: siehe HANDOVER.md

## Claude-Code-Tips
Die 16 Tips (https://raw.githubusercontent.com/aishwaryanr/awesome-generative-ai-guide/main/youtube/claude-code-16-tips.md) wurden am 2026-10-25 durchgegangen; Umsetzung: CLAUDE.md, HANDOVER.md, kaputtes `npm test` entfernt.
