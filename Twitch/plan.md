# Twitch - Trafic élevé

## I. Description

Twitch est une plateforme de streaming qui permet aux utilisateurs de diffuser un flux video en direct et dans le même temps permettre à ceux-ci de visionner un streamer de leur choix. Les viewers peuvent réagir via un chat textuel et ont la possiblité de faire des dons aux streamers pour les encourager à continuer de produire du contenu sur la plateforme : C’est le principal business modèle de la plateforme

### Objectif

L’objectif pour la plateforme est de mettre en avant les streamers les plus populaires pour attirer un maximum de personnes, les faire rester le plus longtemps possible pour créer un esprit communautaire, vaforisant ainsi les donnations monétaires.

### Type d’utilisateur prévus

- Streamer
- Viewer

### Autres informations

Selon les évenements externernes, beaucoup de dont (peu importe le montant) peuvent être effectués en une courte période de temps (pics) ce qui peut faire monter la charge très rapidement

---

## II. Architecture globale

- Chat des viewers fait en langage Go
- Frontend de l'application Web fait en React.js
- Elasticsearch pour trouver les stream en top tendance
- Server et API en Go et Ruby on Rails
- Infrastructure en Amazon Web Services (AWS)
- Plusieurs base de données PostgreSQL et Firebase
- Processus algo en C et C++
- Devops : Jenkins, Terraform, Vanish
- Monitoring : Rollbar, Graphite, Nagios, Ganglia
- Serveurs NGinx

[Mettre un schema ici]

## III - Exigence du test

On estime que twitch à 83 Million de traffic utilisateur / mois
On peut peux donc end déduire un traffic horaire de 115 000 utilisateur / heure
Sachant qu'il y a moins de monde le matin (6h) et beaucoup plus le soir (21h)
En outre on peut s'attendre à 143 000 personnes en traffic le soir, cette dernière valeure servira de référence pour les exigences de tests ci-dessous.

Prenons ici le cas où il y un évenement, on donc qu'on atteint des pic à valeur élevé.

Par exemple :

| Business Transactions           | User Load | Response Time | Transactions per hour |
| ------------------------------- | :-------: | :-----------: | :-------------------: |
| twitch.tv                       |  143 000  |    1.28 s     |        286 000        |
| Envoyer un message dans le chat |  35 000   |   9 à 12 ms   |        70 000         |

## IV - Environnement de test

Machine utilisé : MacBook Pro Intel 16p
Processeur : Intel Core i7
Mémoire : 16Go
Processeur graphique (carte graphique) : AMD Radeon PRO 5300M
Système d'exploitation : MacOS Monterey 12.4
