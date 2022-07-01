# Monbento - Trafic moyen

## I - Préambule

### Desciption

Mon Bento, comme son nom l'indique propose en vente des boites à plusieurs niveaux pour un repas nomade. Issue d’une ingénirerie Française et d’une fabrication française et locale, sa notoriété leur à permis de se diversifier dans des gourdes et d’autre ustensil lié aux bentox.

### Objectif de l'application

L’objectif de leur application web est de vendre un produit déjà fais , de vendre un produit personnalisable ou des pièces de rechange permettant de réparer les box ou les gourdes vendu. 

### Type d’utilisateur prévus

Personne voulant ramener leur déjeuner/repas dans un produit de qualité Française.

- Utilisateur visiteur
- Acheteur

### Autres informations

L’entreprise gagne du trafic et de la popularité lorsque le site est en Solde mais aussi graçe aux collaborations ephemeres comme celle du Petit Prince.

---

## II - **Architecture de l'application**

CMS : Wordpress

Language de programmation : PHP

Framework JavaScript : Framework JavaScript

Serveur Web : Apache

Base de donnée  : MySQL

Live chat : Zendesk

Boutique en ligne : Magento

Régie publicitaire : Microsoft Advertising , Google Ads

## III - Exigence du test

Type de test : Stress test

Suite au solde d’été, nous voulons tester l’aflux d’utilisateur suite à une annonce de promo.

Ce qui causera un pick d’utilisateur suite à cette annonce.

| Business Transactions | User Load | Response Time (ms) | Transactions per hour |
| --- | --- | --- | --- |
| Access to landing page | 5000 | 9-12 | 18 000 |
| Access to list product sold page | 3000 | 9-12 | 15 000 |
|  |  |  |  |

## IV - Environnement de test

Puce Apple M1 Pro

32Go RAM

macOs Monterey 12.4

Aucune idée de l'environnement en production

## V - Planification des tests

Scénario:
S'assurer qu'un achat puisse être réaliser pendant une heure de pointe pendant la période de Noël. Le système doit maintenir un temps de réponse convenable lors des phases d'achat pour conservé un taux de conversion élevé.

- Ramp-up -> 15 Vuser / 10s
- Steady -> 750Vuser - 10min.
- Ramp-down -> 25Vuser / 10s.

Pour simuler la charge et décharge progressive du site en entrée et sortie d'heure de pointe le soir.
	 
Métric à surveiller: Temps de réponse , Average load time ,Wait time, request per seconds.

Les métrics qui définiront la réussite/échec du test sera principalement le temps de réponse pour les entrées ainsi que le wait time pour garder la converstion client.

## VI - Etapes des tests

| Step # | Business Process : Nouveau client  |
|--------------|:-----------:|
| 1 | Home |
| 2 | Cherche un produit |
| 3 | Cherche un produit |
| 4 | Personnalisé son produit |
| 5 | Inscription |
| 6 | Login |
| 7 | Panier |
| 8 | Livraison |
| 9 | Payement |
| 10 | Logout |



| Step # | Business Process : Achat d'un produit |
|--------------|:-----------:|
| 1 | Home |
| 2 | Login |
| 3 | Cherche un produit |
| 4 | Cherche un produit|
| 5 | Personnalisé son produit|
| 6 | Livraison |
| 7 | Payement |
| 8 | Logout |