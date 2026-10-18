---
name: limite
description: >-
  Ménage la limite d'usage de Claude Code : installe deux sous-agents Haiku (Explore pour chercher et lire
  le code, chores pour les corvées mécaniques) et une note CLAUDE.md qui leur envoie le travail facile ;
  Opus garde la conception, le débogage et les modifications sur plusieurs fichiers. À utiliser quand
  l'utilisateur dit « limite », atteint trop vite sa limite Claude, ou veut un modèle moins cher sur les
  tâches simples.
argument-hint: "[--projet]"
disable-model-invocation: true
---

# limite

Claude Code fait tout tourner sur le modèle de la session. Sur Opus, chercher un fichier, lire un journal
ou renommer un import consomme la limite d'usage, et l'agent Explore intégré hérite lui aussi du modèle de
la session. Ce skill envoie le travail facile sur Haiku (`model: haiku`, toujours le Haiku le plus récent).

Ce que l'utilisateur a tapé après `/limite` : `$ARGUMENTS`

## Portée

- Par défaut : tous les projets de l'utilisateur. Les agents vont dans `~/.claude/agents/`, la note dans
  `~/.claude/CLAUDE.md`.
- `--projet` (ou demande explicite pour ce seul projet) : les agents vont dans `.claude/agents/`, la note
  dans `./CLAUDE.md` à la racine du dépôt.

## Étapes

1. Lire `templates/Explore.md` et `templates/chores.md` dans le dossier de ce skill.
2. Pour chacun, regarder le dossier d'agents cible (le créer s'il manque) :
   - absent : l'écrire ;
   - présent et identique : ne rien faire ;
   - présent et différent : montrer la différence et demander avant de remplacer. Jamais d'écrasement
     silencieux.
3. Lire `templates/CLAUDE-note.md`. Si le `CLAUDE.md` cible a déjà une section « Modèles » (ou les mêmes
   règles dans une autre langue), la laisser. Sinon, ajouter la section, traduite dans la langue du reste
   du fichier. Créer le fichier s'il n'existe pas.
4. Dire à l'utilisateur ce qui a été écrit, avec les chemins, puis :
   - redémarrer Claude Code (ou ouvrir `/agents`) pour charger les nouveaux agents ;
   - vérifier dans `/agents` qu'Explore et chores affichent bien Haiku ;
   - la session elle-même reste sur Opus, seul le travail délégué passe sur Haiku.

## Notes

- Un agent utilisateur nommé `Explore` remplace l'agent intégré : c'est voulu.
- Haiku convient pour chercher, lire et faire une modification d'une ligne. Ce qui demande du jugement
  reste sur Opus : chores s'arrête de lui-même quand une tâche touche plus de 2 fichiers ou demande une
  décision de conception.
- Anthropic ne publie pas le poids de chaque modèle dans la limite d'un abonnement, seulement qu'Opus en
  consomme beaucoup plus que Sonnet, et Sonnet plus que Haiku. Ne promettre aucun chiffre.

## Provenance

Adapté du skill `limite` de Melvynx (paquet npm `aiblueprint-cli` 1.4.111, dossier
`agents-config/skills/limite`, licence MIT, auteur « AIBlueprint »), lu en entier avant reprise : aucun
appel réseau, aucun script. Adaptations Xcellence : traduction française ; agents en lecture seule pour
Explore ; ni commit, ni push, ni fusion, ni migration, ni appel à la production, à Amazon ou Ads, ni à un
service payant pour chores ; fichiers sensibles du SaaS jamais lus, secrets jamais recopiés. Déjà appliqué
au dépôt Amazon-app (`.claude/agents/`, `CLAUDE.md`), branche `claude/keen-goodall-75quf6-limite`.
