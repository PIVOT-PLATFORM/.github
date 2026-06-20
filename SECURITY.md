# Security Policy — PIVOT Platform

Politique de sécurité **umbrella** pour tous les repositories PIVOT Platform.

---

## Signaler une vulnérabilité

**Ne pas ouvrir d'issue publique GitHub pour une vulnérabilité de sécurité.**

Une divulgation publique avant qu'un correctif soit disponible expose tous les utilisateurs PIVOT.

Utiliser **GitHub Private Vulnerability Reporting** dans le repo concerné :

| Composant affecté | Lien de signalement |
|-------------------|---------------------|
| API REST · Spring Security · JWT · BDD | [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core/security/advisories/new) |
| Frontend Angular · Auth OIDC · XSS · CSP | [pivot-ui](https://github.com/PIVOT-PLATFORM/pivot-ui/security/advisories/new) |
| Incertitude sur le composant | [pivot-core](https://github.com/PIVOT-PLATFORM/pivot-core/security/advisories/new) (par défaut) |

---

## Délais de réponse

| Étape | Objectif |
|-------|----------|
| Accusé de réception | 48 heures |
| Évaluation initiale | 5 jours ouvrés |
| Correctif — Critique (CVSS ≥ 9.0) | 7 jours |
| Correctif — Élevé (CVSS 7.0–8.9) | 30 jours |
| Correctif — Moyen / Faible | Prochaine release planifiée |

---

## Politique de divulgation coordonnée

1. Signalement via advisory privé
2. Accusé de réception + évaluation sévérité
3. Correctif développé sur branche privée
4. Release + advisory publié avec CVE si applicable
5. Rapporteur crédité (sauf anonymat demandé)

---

## Scanning actif en CI

Tous les repos PIVOT maintiennent :

| Outil | Couverture |
|-------|-----------|
| Gitleaks | Secrets dans le code et l'historique git |
| CodeQL | SAST — Java (pivot-core) · JavaScript/TypeScript (pivot-ui) |
| Semgrep | OWASP Top 10, injection, XSS, JWT, secrets |
| Trivy | SCA — dépendances Maven + npm |
| Plumber | Conformité et hardening des workflows CI/CD |
| OpenSSF Scorecard | Score de sécurité open-source global |
| ZAP DAST | Scan dynamique API (pivot-core) |

---

## Versions supportées

| Version | Support |
|---------|---------|
| dernière release | ✅ Support complet |
| dernière - 1 | ✅ Correctifs sécurité uniquement |
| antérieures | ❌ Aucun support |
