# Terraform Quick Docs (VS Code Extension)

Marketplace: `LemurDaniel.terraform-quick-docs` · Repo: LemurDaniel/VSCode__terraform_quick_docs

## Stack & Befehle
- JS (client = VS Code Extension, server = Language Server), webpack
- `npm install` (postinstall installiert client/server), `npm run lint`, `npm run package`
- Kein Testframework vorhanden

## Release
- Pipeline `.github/workflows/package.yaml` (`workflow_dispatch`, `skip_publish=false` auf master): vsce package → publish → GitHub Release inkl. `.vsix`
- Release-Notes kommen aus dem CHANGELOG-Abschnitt `## [<version>]`; Version in package.json + package-lock.json + CHANGELOG pflegen
- Provider-Updates laufen automatisch (`providerCheck.yaml`)

## Konventionen
- Commits: Name `LemurDaniel`, Mail `landau.daniel.1998@gmail.com`
- Offene Sichtbarkeits-Themen: siehe HANDOVER.md

## Claude-Code-Tips
Die 16 Tips (https://raw.githubusercontent.com/aishwaryanr/awesome-generative-ai-guide/main/youtube/claude-code-16-tips.md) wurden am 2026-10-25 durchgegangen; Umsetzung: CLAUDE.md, HANDOVER.md, kaputtes `npm test` entfernt.
