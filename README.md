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

`pivot-core`, `pivot-ui` et `pivot-docs` ont leurs propres fichiers communautaires qui
**surchargent** ceux-ci. Depuis la bascule Spring Modulith (ADR-030), les domaines métier
(agilité, collaboratif) sont des **modules internes** du Socle et non plus des repos séparés —
les anciens repos `pivot-{agilite,collaboratif,pilotage}-{core,ui}` et `pivot-design-system`
sont **archivés**. Les fichiers de ce repo s'appliquent aux repos d'outillage restants
(`pivot-cicd`, `pivot-infra`, `pivot-benchmarks`) sauf surcharge locale.

## Protection

- CODEOWNERS : tout changement nécessite une review (@ApoSkunz, @0bno, @Destinea, @tellebma, @leo-brgn)
- Plumber : conformité CI/CD vérifiée sur les workflows de ce repo
