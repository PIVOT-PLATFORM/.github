# Contributing to PIVOT Platform

PIVOT est une suite collaborative open-source — outils activables par les admins, auto-hébergeable, sans lock-in SaaS.

> Ce fichier est le guide de contribution **par défaut** pour tous les repositories PIVOT.
> Chaque repo peut avoir son propre `CONTRIBUTING.md` plus spécifique.

---

## Repositories

| Repo | Pour contribuer à |
|------|------------------|
| [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core/blob/main/CONTRIBUTING.md) | Backend Java · API REST · BDD · Sécurité |
| [pivot-ui](https://github.com/PIVOT-PLATFORM/pivot-ui/blob/main/CONTRIBUTING.md) | Frontend Angular · Composants · Accessibilité |
| [pivot-docs](https://github.com/PIVOT-PLATFORM/pivot-docs) | Documentation générale |

---

## Règles communes à tous les repos

### Avant de contribuer

1. Ouvrir une issue dans le repo concerné
2. Attendre l'accord d'un mainteneur avant de démarrer une implémentation non triviale
3. Lire le `CONTRIBUTING.md` spécifique au repo ciblé

### Branches

```
feat/us-{id}-{slug}   Nouvelle fonctionnalité
fix/{id}-{slug}       Correction de bug
chore/{slug}          CI, deps, config
docs/{slug}           Documentation
```

### Commits

Format **Conventional Commits** : `type(scope): message`

Co-author obligatoire si IA utilisée : `Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>`

### Pull Requests

- CI doit être verte avant merge
- Review @ApoSkunz obligatoire
- Label `security` ou `breaking-change` → review humaine obligatoire

---

## Vulnérabilités de sécurité

**Ne pas ouvrir d'issue publique.** Voir [SECURITY.md](SECURITY.md).

---

## Code de conduite

Voir [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
