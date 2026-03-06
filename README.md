# renovate-demo-app

Demo-Repository für den **Renovate Bot Workshop** bei CrowdCode.

> Dieses Repository enthält **absichtlich veraltete Dependencies** – das ist kein Versehen, sondern Absicht! Hier wird geübt, Renovate einzurichten und zu konfigurieren.

## Enthaltene Abhängigkeiten (bewusst veraltet)

### Node.js (`package.json`)

| Paket | Im Repo | Aktuell (ca.) |
|-------|---------|---------------|
| `express` | 4.17.1 | 4.21.x / 5.x |
| `axios` | 0.21.1 | 1.x (Major!) |
| `lodash` | 4.17.15 | 4.17.21 |
| `eslint` | 7.32.0 | 9.x |
| `jest` | 27.5.1 | 29.x |

### Java/Maven (`pom.xml`)

| Paket | Im Repo | Aktuell (ca.) |
|-------|---------|---------------|
| Spring Boot | 2.5.0 | 3.x (Major!) |
| Guava | 30.0-jre | 33.x |
| Commons Lang 3 | 3.11 | 3.14.x |

## Übungsablauf

Dieses Repo wird in allen Übungen des Workshops verwendet:

1. **Übung 1** – Renovate GitHub App installieren, dieses Repo forken
2. **Übung 2** – Erste `renovate.json` mit `config:recommended` erstellen
3. **Übung 3** – `packageRules`: Updates bündeln und filtern
4. **Übung 4** – Automerge für Patch-Updates konfigurieren
5. **Übung 5** – Scheduling: Wann soll Renovate laufen?
6. **Übung 6** *(optional)* – Self-hosted Renovate per Docker

## CI-Pipeline

Das Repo enthält eine GitHub Actions Pipeline (`.github/workflows/ci.yml`), die bei jedem Pull Request läuft.

**Das ist wichtig für Übung 4 (Automerge):** Renovate merged Pull Requests nur dann automatisch, wenn alle Status-Checks grün sind. Ohne laufende CI würde Automerge nie auslösen.

## Erste Schritte

1. Dieses Repository forken
2. Renovate App installieren: [github.com/apps/renovate](https://github.com/apps/renovate)
3. Den Onboarding-PR von Renovate beobachten

Eine `renovate.json` gibt es hier bewusst **nicht** – die erstellen wir gemeinsam in Übung 2.