# Handover: Sichtbarkeit Terraform Quick Docs

Stand: 2026-10-25

## Erledigt
Icon, Social-Preview-PNG, Marketplace-Metadaten, README-Badges, Issue-Templates, Release-Step in der Pipeline, GitHub Description + Topics, Version 1.0.13.

## Offen
1. Social Preview manuell hochladen (`.img/social-preview.png`, GitHub Settings)
2. Pipeline auslösen: `gh workflow run "Package or Publish to Marketplace" -f skip_publish=false --ref master`, dann `gh run watch`. Noch nie gelaufen. Scheitert der Release-Step, ist der Publish schon durch → Release manuell: `gh release create v1.0.13 <vsix> --notes-file …`
3. Marketplace-Seite prüfen (Icon, Badges, Banner)
4. Rating-Badge ergänzen, sobald Reviews existieren: `https://vsmarketplacebadges.dev/rating-short/LemurDaniel.terraform-quick-docs.svg`
5. Open VSX (`npx ovsx publish`, Secret `OVSX_PAT`)
6. Review-Hinweis in der Extension (einmalig nach ~20 Nutzungen)
7. Alt-Releases nachtragen (keine Tags vorhanden)
8. Extern: Awesome-Listen, Reddit, dev.to, LinkedIn
