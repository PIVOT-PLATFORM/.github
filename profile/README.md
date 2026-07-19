# PIVOT Platform

**Suite collaborative open-source** — outils activables par les administrateurs, auto-hébergeables, sans lock-in SaaS.

Rendre accessible à tous (associations, TPE/PME, entreprises) des outils collaboratifs de qualité : tableau blanc temps réel, sessions live, roadmap/Gantt, quiz gamifié.

---

## Architecture — Spring Modulith

Depuis la bascule **Spring Modulith** (ADR-030), les domaines métier vivent comme **modules internes**
du Socle plutôt que dans des repos séparés : `pivot-core` embarque les modules backend, `pivot-ui`
embarque le design system et les libs frontend dans un workspace Angular unique. Un seul déploiement,
frontières de modules vérifiées par tests, isolation des données conservée par schéma PostgreSQL.

## Repositories

### Socle

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core) | Backend API REST · BDD · Sécurité · Système de modules · **modules métier internes** (agilité, collaboratif) | Java 25 · Spring Boot 4 · Spring Modulith · PostgreSQL · Flyway |
| [pivot-ui](https://github.com/PIVOT-PLATFORM/pivot-ui) | Frontend réactif · Modules lazy-loaded · WCAG 2.1 AA · **design system + libs modules** (workspace Angular) | Angular 22 · TypeScript · SCSS · Storybook · Vitest · Playwright |
| [pivot-docs](https://github.com/PIVOT-PLATFORM/pivot-docs) | Documentation générale, ADR, backlog | Markdown |

### Modules métier

Les domaines sont désormais des **modules internes** — voir ADR-030 :

| Domaine | Où | Fonctionnalités |
|---------|-----|-----------------|
| **Agilité** | module interne `pivot-core/agilite/` + workspace `pivot-ui` | Scrum poker, rétrospectives, roues d'équipe, daily standup |
| **Collaboratif** | module interne `pivot-core/collaboratif/` + workspace `pivot-ui` | Tableau blanc temps réel, quiz, sessions live, formulaires |
| **Pilotage** | extrait de PIVOT (produit distinct) | Roadmap/Gantt, portefeuille de projets — voir `pivot-core/PILOTAGE-HANDOFF.md` |

Chaque module reste **activable individuellement** par les administrateurs de tenant et isole ses
données dans un schéma PostgreSQL dédié.

> Les anciens repos `pivot-{agilite,collaboratif,pilotage}-{core,ui}` et `pivot-design-system` sont
> **archivés** (contenu absorbé par le Socle) et conservés en lecture seule pour l'historique.

### Outillage & Infrastructure

| Repo | Description | Stack |
|------|-------------|-------|
| [pivot-cicd](https://github.com/PIVOT-PLATFORM/pivot-cicd) | Source unique des pipelines CI/CD (reusable workflows + composite actions) de l'organisation | GitHub Actions |
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
