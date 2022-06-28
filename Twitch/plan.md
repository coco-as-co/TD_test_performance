# Site large : Twitch

## 1. Description

Twitch est une plateforme de streaming qui permet aux utilisateurs de diffuser un flux video en direct et dans le même temps permettre à ceux-ci de visionner un streamer de leur choix. Les viewers peuvent réagir via un chat textuel et ont la possiblité de faire des dons aux streamers pour les encourager à continuer de produire du contenu sur la plateforme : C’est le principal business modèle de la plateforme

### Objectif

L’objectif pour la plateforme est de mettre en avant les streamers les plus populaires pour attirer un maximum de personnes, les faire rester le plus longtemps possible pour créer un esprit communautaire, vaforisant ainsi les donnations monétaires.

### Type d’utilisateur prévus

- Streamer
- Viewer

### Autres informations

Selon les évenements externernes, beaucoup de dont (peu importe le montant) peuvent être effectués en une courte période de temps (pics) ce qui peut faire monter la charge très rapidement

---

## 2. Architecture globale

- Chat des viewers fait en langage Go
- Frontend de l'application Web fait en React.js
- Elasticsearch pour trouver les stream en top tendance
