# Roles et Definition of Done

## Roles (4)

| Role | Responsabilites | Membre |
|------|-----------------|--------|
| Product Owner / Scrum Master | Priorise le backlog Notion, anime sprint planning et retro, suit les metriques DORA | _a completer_ |
| Dev Backend / API | Code FastAPI (`app/`), tests (`tests/`), endpoints `/health`, `/ready`, `/predict` | _a completer_ |
| DevOps / Plateforme | CI GitHub Actions, Dockerfile, docker-compose, K8s, monitoring | _a completer_ |
| ML / IA | Pipeline `ml/`, agent `agent/`, revue des sorties generees par l'IA | _a completer_ |

Les roles tournent a chaque sprint ; chacun reste relecteur d'au moins une PR.

## Definition of Done

Une carte passe en **Termine** seulement si :

- [ ] **Tests verts** : `pytest` passe en local et dans la CI
- [ ] **Lint OK** : `ruff check .` sans erreur sur les fichiers modifies
- [ ] **Revue faite** : au moins une approbation d'un autre membre sur la PR
- [ ] **Doc a jour** : README / docs modifies si le comportement change
- [ ] **Aucun secret** : ni `.env`, ni jeton, ni mot de passe dans le diff
- [ ] **Lien PR** renseigne dans la carte Notion

## Regle IA

L'IA propose, l'humain valide : lint, tests et plan sont toujours executes avant de merger du code ou un backlog generes par IA.
