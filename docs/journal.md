# Journal

Format : date — ce qui a été installé ou réglé — droits donnés — comment le retirer.

## 2026-11-02 — Audit de départ (aucune installation)

Rien n'a été installé ni activé. Relevé de l'état du compte pour servir de référence.

**Connecteurs réellement branchés** (relevé automatique, pas déclaratif) :

| Connecteur | État | Droits d'écriture présents | Retrait |
|---|---|---|---|
| Gmail | connecté | envoi, réponse, transfert, corbeille, spam, labels | Customize > Connectors > Gmail > déconnecter |
| Notion | connecté | création/modification/suppression de pages et bases, commentaires | idem |
| Canva | connecté | création/édition/export/publication de designs | idem |
| Netlify | connecté | déploiement et modification de projets (`*-updater`) | idem |
| Slack | connexion incomplète | — (inactif) | terminer ou supprimer |

GitHub n'apparaît pas comme connecteur MCP : c'est l'app GitHub utilisée par Claude Code.
Portée GitHub de cette session : `tomdeniau0717-star/max` uniquement.

**À vérifier côté utilisateur** : que l'app GitHub est installée sur « Only select repositories »
et n'inclut pas le dépôt snackly (https://github.com/apps/claude/installations/select_target).

## 2026-11-02 — Décisions

- **CLAUDE.md** : ajout de la règle de format (10 lignes max, une question ou action à la fois).
- **App GitHub** : reste installée sur `snackly`, `kebab-beyo-pizza`, `max` — choix assumé,
  nécessaire aux sessions Clickom. Cloisonnement assuré par les règles du CLAUDE.md, pas par
  la portée GitHub. Retrait : https://github.com/apps/claude/installations/select_target
- **Netlify** : non lié à Clickom, déconnecté par l'utilisateur.
- **Slack** : connexion incomplète supprimée par l'utilisateur.

## 2026-11-02 — Installation acceptée : yt-dlp

- **Quoi** : paquet PyPI officiel `yt-dlp`, version 2026.10.26, installé par `pip3 install yt-dlp`
  dans le conteneur de session cloud (pas sur la machine de l'utilisateur).
- **Pourquoi** : lire des vidéos TikTok (sous-titres + images extraites avec ffmpeg).
- **Droits donnés** : aucun. Lit des URL publiques, écrit dans le dossier temporaire de session.
  Aucun identifiant, aucun cookie. Condition posée : ne jamais demander les identifiants TikTok.
- **ffmpeg** : déjà présent (6.1.1), aucune installation supplémentaire.
- **Retrait** : `pip3 uninstall yt-dlp`, ou rien — le conteneur est effacé en fin de session.

## 2026-11-06 — Installation acceptée : plugin frontend-design

- **Quoi** : plugin `frontend-design` v1.1.1, éditeur Anthropic (officiel), 1 skill.
- **Pourquoi** : interfaces plus travaillées quand Claude dessine un écran (site Clickom, Track).
- **Droits donnés** : aucun — « ajoute uniquement des instructions pour Claude ».
- **Où** : claude.ai → Paramètres → Plug-ins, donc actif sur toutes les sessions.
- **Retrait** : même page, interrupteur à droite du nom.

## 2026-11-06 — Installations acceptées : trois plugins (Paramètres → Plug-ins)

| Plugin | Éditeur | Version | Contenu | Synchro auto |
|---|---|---|---|---|
| Agent skills | Addy Osmani (tiers, MIT) | 0.6.15 | 25 skills, 9 commandes, 4 agents, hooks de cache doc (audités) | off |
| i-have-adhd | ayghri (tiers, MIT) | — | 1 skill, hook de démarrage opt-in (audité) | off |
| Security Guidance | Anthropic (officiel) | 2.0.17 | 5 hooks : alertes à l'édition, revue du diff à l'arrêt, revue des commits | — |

- **Droits donnés** : aucun accès aux comptes. Les trois « peuvent exécuter du code sans demander » dans les sessions locales (Cowork) — scripts lus, sans réseau sortant hors pages déjà consultées.
- **Quota** : Security Guidance lance une revue IA à chaque arrêt de réponse → consommation en hausse.
- **Retrait** : Paramètres → Plug-ins → interrupteur. Marketplaces : Gérer les marketplaces.
- **Refusés** après audit : Graphify, claude-mem, C1, Superpowers (doublon), Context7, agrégateur MCP, Flare, Strix.

## 2026-11-06 — Rangement des dépôts (état en fin de journée)

- **Créé** : `clickom-mentors` (juridique + commercial, 66 fichiers, CLAUDE.md racine, code Clickom en lecture seule). Les deux conversations mentors tournent dessus.
- **Archivés par Tom** : `clickom-legal-mentor`, `clickom-commercial-menthor-`. Anciennes conversations encore à archiver dans la barre latérale.
- **Décision** : `apps` à supprimer (copies seulement), `track` et courses gardent chacun leur dépôt ; courses à renommer `family`. Mentor technique reste dans `kebab-beyo-pizza`.
- **À faire demain** : tableau de bord (artefact), plugins par dépôt (impossible en cloud — un seul jeu par compte), ligne « clickom-mentors en lecture seule » dans le CLAUDE.md de `snackly`.
- **Toujours ouvert** : clé Gemini dans Track, Netlify et Vercel à repointer, Gmail/Notion permissions.
