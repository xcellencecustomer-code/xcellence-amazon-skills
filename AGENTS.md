# Consignes pour les agents

## Tests et GitHub Actions

Décision de Yusuf (17/10/2026, rendue permanente le 20/10/2026, ADR 001 d'`xcellencecustomer-code/Amazon-app`) : les vérifications tournent en local ou dans la session Claude Code, jamais sur les minutes GitHub Actions.

- Ce dépôt n'a aucun workflow et n'en a pas besoin : ne pas créer de `.github/workflows/` sans GO explicite de Yusuf.
- Si un workflow devient un jour nécessaire (GO de Yusuf), il ne se lance qu'à la main (`workflow_dispatch`), jamais sur `push`, `pull_request` ou `schedule`.
- Vérifier soi-même avant de pousser (relecture des `SKILL.md` modifiés, liens vers `references/` valides).
