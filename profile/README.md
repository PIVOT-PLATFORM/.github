# PIVOT Platform

**Suite collaborative open-source** — outils activables par les administrateurs, auto-hébergeables, sans lock-in SaaS.

Rendre accessible à tous (associations, TPE/PME, entreprises) des outils collaboratifs de qualité : tableau blanc temps réel, sessions live, roadmap/Gantt, quiz gamifié.

---

## Repositories

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core) | Backend API REST · BDD · Sécurité · Système de modules | Java 25 · Spring Boot 4 · PostgreSQL · Liquibase |
| [pivot-ui](https://github.com/PIVOT-PLATFORM/pivot-ui) | Frontend réactif · Modules lazy-loaded · WCAG 2.1 AA | Angular 22 · TypeScript · SCSS · Vitest · Playwright |
| [pivot-docs](https://github.com/PIVOT-PLATFORM/pivot-docs) | Documentation générale du projet | Markdown |

---

## Modules prévus

| Module | Description |
|--------|-------------|
| `whiteboard` | Tableau blanc collaboratif temps réel |
| `session` | Sessions live — QUIZ, POLL, WORDCLOUD, BRAINSTORM, Q&A |
| `roadmap` | Roadmap / Gantt intégré |
| `survey` | Système de sondage |
| `quiz` | Quiz interactif gamifié |

Chaque module est **activable individuellement** par les administrateurs de tenant.

---

## Principes

- **Auto-hébergeable** — Docker Compose, pas de dépendance cloud
- **OIDC-compatible** — Keycloak, Azure AD, Okta, tout IdP standard
- **Multi-tenant** — isolation des données par organisation
- **AGPL-3.0** — améliorer PIVOT et le déployer en SaaS = publier les modifications

---

## Contribuer

Lire [CONTRIBUTING.md](../CONTRIBUTING.md) puis ouvrir une issue dans le repo concerné.

Signalement de vulnérabilité → [SECURITY.md](../SECURITY.md).
