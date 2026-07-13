# PIVOT Platform

**Suite collaborative open-source** — outils activables par les administrateurs, auto-hébergeables, sans lock-in SaaS.

Rendre accessible à tous (associations, TPE/PME, entreprises) des outils collaboratifs de qualité : tableau blanc temps réel, sessions live, roadmap/Gantt, quiz gamifié.

---

## Repositories

### Socle

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core) | Backend API REST · BDD · Sécurité · Système de modules | Java 25 · Spring Boot 4 · PostgreSQL · Liquibase |
| [pivot-ui](https://github.com/PIVOT-PLATFORM/pivot-ui) | Frontend réactif · Modules lazy-loaded · WCAG 2.1 AA | Angular 22 · TypeScript · SCSS · Vitest · Playwright |
| [pivot-design-system](https://github.com/PIVOT-PLATFORM/pivot-design-system) | Composants, tokens, patterns · Angular CDK (a11y) + SCSS BEM custom · aucune lib visuelle tierce (ADR-007) | Angular CDK · SCSS · Storybook |
| [pivot-docs](https://github.com/PIVOT-PLATFORM/pivot-docs) | Documentation générale, ADR, backlog | Markdown |

### Domaines (phase 3)

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-pilotage-core](https://github.com/PIVOT-PLATFORM/pivot-pilotage-core) / [-ui](https://github.com/PIVOT-PLATFORM/pivot-pilotage-ui) | Roadmap/Gantt, portefeuille de projets, ADR projet | Java 25 · Spring Boot 4 / Angular |
| [pivot-agilite-core](https://github.com/PIVOT-PLATFORM/pivot-agilite-core) / [-ui](https://github.com/PIVOT-PLATFORM/pivot-agilite-ui) | Capacity planning, daily standup, scrum poker | Java 25 · Spring Boot 4 / Angular |
| [pivot-collaboratif-core](https://github.com/PIVOT-PLATFORM/pivot-collaboratif-core) / [-ui](https://github.com/PIVOT-PLATFORM/pivot-collaboratif-ui) | Whiteboard, quiz, sessions live, formulaires | Java 25 · Spring Boot 4 / Angular |

Chaque module est **activable individuellement** par les administrateurs de tenant. Les repos domaines
partagent le même schéma PostgreSQL (isolé par schéma dédié) et consomment `pivot-core-starter` /
`@pivot/ui-core` publiés par le Socle.

### Outillage & Infrastructure

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-template-core](https://github.com/PIVOT-PLATFORM/pivot-template-core) / [-ui](https://github.com/PIVOT-PLATFORM/pivot-template-ui) | Template repositories GitHub pour scaffolder un nouveau module (`pivot-{module}-core` / `-ui`) | Spring Boot 4 / Angular |
| [pivot-infra](https://github.com/PIVOT-PLATFORM/pivot-infra) | Infrastructure as Code — provisioning de l'hôte GCP de référence (VM Docker Compose) | Terraform · GCP |
| [pivot-benchmarks](https://github.com/PIVOT-PLATFORM/pivot-benchmarks) | Analyses fonctionnelles du marché, en entrée de conception des produits | Markdown · Docusaurus |

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
