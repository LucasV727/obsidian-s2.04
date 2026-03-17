# Sujet de la SAE : Influence des Réseaux Sociaux

## Présentation du Corpus
Adil Shamim a publié sur **Kaggle** une enquête portant sur l’usage des réseaux sociaux par les étudiants et son influence sur la santé mentale, leurs études et leurs relations personnelles.

Le fichier `Student’s Social Media Addiction.csv` contient des données anonymisées :
- **Population :** Étudiants de 16 à 25 ans.
- **Période :** 1er trimestre 2025.
- **Géographie :** Couverture internationale.
- **Niveaux d'études :** Lycéen, étudiant, diplômé.

---

## Détails de l'Enquête

### 1. Identité
- Identifiant, âge, genre.
- Niveau scolaire, pays de résidence.
- Situation familiale (célibataire, en couple, autre).

### 2. Réseaux Sociaux & Vie Privée
- Temps quotidien moyen (heures).
- Plateforme la plus utilisée.
- Influence sur les résultats scolaires.
- Heures de sommeil par nuit.
- Score de santé mentale (1 à 10).
- Nombre de conflits interpersonnels.
- **Score d’addiction** (1 à 10, échelle de Bergen).

### 3. Validation & Nettoyage
- Vérification des champs obligatoires et des plages de valeurs (ex: 0-24h).
- Déduplication via les identifiants.
- Anonymisation complète (RGPD compliance).

---

## Cahier des Charges de l'Application APEX
**Titre :** *L'usage des réseaux sociaux influence-t-il les résultats scolaires ?*

### Page 1 : Accueil
- [x] **Titre :** Tableau de bord développé par [Noms Prénoms].
- [x] **Description :** Texte dynamique présentant les stats (X étudiants, âge de A à B, dans C pays) calculées à partir des données.
- [x] **Graphique :** Diagramme à barres des 5 réseaux sociaux les plus utilisés (tri décroissant).

### Page 2 : Corpus (Rapport Dynamique)
Affichage de toutes les colonnes (titres en français), trié par score d'addiction.
- [x] **État principal :** Tri addiction croissant, toutes les lignes sur une page.
- [x] **Thème "Réussite" :** Surlignage vert (étudiants sans influence négative sur les résultats), tri par ID.
- [x] **Thème "Diplôme" :** Camembert représentant le nombre d'étudiants par catégorie.
- [x] **Thème "Lien Addiction-Sommeil" :** Temps de sommeil moyen par degré d'addiction.
- [x] **Rapport personnalisé :** Un rapport au choix (justifié par sa pertinence).

### Page 3 : Exploration
- [x] Rapport avec **facettes** (Faceted Search).
- [x] Possibilité de recherche sur tous les attributs de la table.

### Page 4 : Tableau de bord (Visualisations)
Au moins 5 graphiques pertinents pour représenter le corpus :
- [x] Répartition Homme/Femme.
- [x] Niveaux académiques.
- [x] Pays d'origines.
- [x] Heures passées sur les réseaux.
- [x] Répartition des plateformes.

### Page 5 : Résultats scolaires
- [x] **Graphique dédié :** Nombre d'heures passées sur les réseaux en fonction du taux d'addiction.
- [x] **Contrainte :** Titres obligatoires pour tous les axes (abscisses et ordonnées).

![[Pasted image 20260224173327.png]]
### Page 6 : un **rapport interactif** nommée **IUT** comportant toutes les données des personnes dont le pays est "IUT". Le nom du pays n'apparait pas et le rapport est trié par numéro d'étudiant.

Ce rapport liste **5 états publics nommés** :

- [x] - État principal : le rapport trié par degré d'addiction croissant et affiche TOUTES les lignes de la table sur une seule page.
     - [x] Thème "Réussite" : surligner en vert les étudiants qui déclarent que les réseaux sociaux n'ont pas d'influence sur leurs résultats scolaires, trié par identifiant d'étudiant.
    - [x] Thème "Diplôme" : un camembert représentant le nombre d'étudiants par catégorie de diplôme
    - [ ] Thème "lien addiction-sommeil" : liste le temps moyen de sommeil des étudiants en fonction de leur degré d'addiction.
    - [x] Un rapport de votre choix (dont vous devrez justifier la pertinence).

---

### Page 7 : une nouvelle page **Tableau de bord** présentant les données brutes de l'IUT à l'aide de différents graphiques. 
- [x] Nous souhaitons au moins 5 graphiques : 
- [x] répartition homme/femme, 
- [x] niveaux académiques, 
- [x] pays d'origines, 
- [x] nombre d'heures passées sur les réseaux sociaux, 
- [x] répartition des plateformes utilisées, 
- [x] etc...

ATTENTION ! Nous vous demandons de choisir le graphique qui sera le plus pertinent pour représenter les données du corpus.

---

### Page 8 : une page **Exploration** 
présentant un rapport avec les facettes sur les données du sondage de l'IUT, 
- [x] avec possibilité de faire des recherches sur tous les attributs de la table. 
- [x] Les colonnes du rapports sont celles de la Page 2.
- [ ] il manque quelques column

---

### Page 9 : une page **Addiction** présentant deux [diagrammes](https://en.wikipedia.org/wiki/Line_chart) montrant

- [x] le nombre d'heures passés sur les réseaux sociaux en fonction de leur taux d'addiction.
- [x] les niveaux d'addiction en fonction du réseau social utilisé.

>[!warning]
> ATTENTION ! Nous vous demandons de choisir les graphiques qui seront le plus pertinent pour ces représentations.
  élevé, facile à défendre.

1. Sleep hours per night (dodo) $\leftrightarrow$ mental health score (r=0.55)
2. Addiction ↔ Mental Health (r = -0.67) — la plus impactante socialement. Plus le score d'addiction monte, plus la santé mentale se dégrade. C'est le lien direct "usage excessif → conséquences sur la santé" qui donne du poids à l'analyse.
  
![[1_correlation_matrix 1.png]]
  
---

### Page 10 : une page **personnelle** présentant une comparaison des ATTENTION ! 

>[!warning]
> Nous vous demandons de choisir les graphiques qui seront le plus pertinent pour ces représentations. 
> Les données initiales et de celles que vous venez d'ajouter à votre base de données, permettant de faire ressortir les éléments communs et les différences.

---
## partie final

Nous avons récupéré les résultats scolaires et les notes des étudiants ayant participé à l'enquête. 

Vous devez maintenant :

- mettre à jour votre base de données en ajoutant deux nouvelles tables (résultats et notes)
- analyser s'il existe une corrélation entre les résultats scolaires, les notes et les résultats du sondage

Nous vous demandons de créer une nouvelle page explorant les différentes corrélation possibles afin de pouvoir faire votre analyse. 

**L'originalité et la pertinence** de votre étude **seront fortement valorisées.**