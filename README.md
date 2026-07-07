# .github — PIVOT Platform

Ce repository contient les **fichiers communautaires par défaut** de l'organisation PIVOT Platform.

Les fichiers ici s'appliquent à tous les repositories de l'organisation qui n'ont pas leur propre version.

## Contenu

| Fichier | Rôle |
|---------|------|
| `profile/README.md` | Profil affiché sur la page GitHub de l'organisation |
| `CONTRIBUTING.md` | Guide de contribution par défaut |
| `CODE_OF_CONDUCT.md` | Code de conduite |
| `SECURITY.md` | Politique de sécurité umbrella |
| `SUPPORT.md` | Canaux de support |

## Repositories spécifiques

`pivot-core`, `pivot-ui`, `pivot-docs` et `pivot-collaboratif-core`/`-ui` ont leurs propres fichiers
qui **surchargent** ceux-ci. `pivot-pilotage-core`/`-ui` et `pivot-agilite-core`/`-ui` n'en ont pas
encore (scaffoldés récemment, voir leur `TODO-SETUP.md`) — ce sont les fichiers de ce repo qui
s'appliquent pour l'instant.

## Protection

- CODEOWNERS : tout changement nécessite une review (@ApoSkunz, @0bno, @Destinea, @tellebma, @leo-brgn)
- Plumber : conformité CI/CD vérifiée sur les workflows de ce repo
