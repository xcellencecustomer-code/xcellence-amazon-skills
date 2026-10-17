# Règles Xcellence pour le skill security-audit

Ces règles s'appliquent en plus de `SKILL.md` et l'emportent sur lui en cas de conflit.

## Provenance

- Source : https://github.com/cloudflare/security-audit-skill, dossier `skills/security-audit/`.
- Commit : `c1c8a8c1471069fb0e188eeaff69b8e8db6564a8` (14/09/2026).
- Licence : MIT, Cloudflare, Inc. (`LICENSE`).
- Copie à l'identique. Seul ajout dans `SKILL.md` : le renvoi vers ce fichier, sous le titre. Ajouts propres à Xcellence : ce fichier et `agents/openai.yaml`.
- Relecture avant intégration, le 17/10/2026 :
  - les 22 fichiers ont été lus en entier ;
  - aucune instruction cachée, aucune exfiltration, aucun appel réseau ;
  - les deux validateurs `.cjs` ne font que lire, et leurs tests passent (34/34 et 31/31).
- Mise à jour : reprendre la copie depuis un commit amont précis, refaire la même relecture, puis changer le commit indiqué ici. Jamais de `npx skills add` direct dans l'écosystème.

## Règles d'usage

1. **Mode guidance par défaut.** Le mode audit complet suppose une demande explicite de Yusuf ou du CEO, avec trois éléments :
   - le dépôt cible ;
   - le dossier de sortie ;
   - le budget en nombre d'agents.
2. **Dossier de sortie explicite.** Jamais la valeur par défaut `~/security-audit-skill/...`. Utiliser le scratchpad de la session ou un dossier ignoré par git désigné dans la demande.
3. **Secrets jamais recopiés.** Un secret trouvé (mot de passe, jeton, clé, `.env`, `*.pem`, historique git) est décrit seulement par son fichier, sa ligne, son type et ses 4 premiers caractères suivis de `…`. Il n'apparaît jamais en entier dans `findings.json`, `REPORT.md`, un commentaire GitHub ou un message. Ne pas lire `apps/web/.env.example`, `.secret-guard-baseline` ni `.secret-guard-history-baseline`.
4. **Source seule par défaut.** Le code de la cible n'est pas exécuté (build, tests, fuzzers, navigateur), sauf dans un bac à sable réel :
   - sans réseau ;
   - sans identifiants ;
   - sans accès à Coolify ni au jeton `gh`.

   Sans ce bac à sable, la piste reste en `needs_validation`, comme le prévoit le skill.
5. **Aucune action extérieure.** Pas d'appel aux API Amazon ou Ads, à la production, à un service payant. Pas de push, pas de commentaire public d'un constat non vérifié.
6. **Restitution.** Les constats `confirmed` vont au CEO dans #44, avec leur preuve source. Toute correction suit le circuit habituel : branche, revue indépendante, PR, GO de Yusuf.
