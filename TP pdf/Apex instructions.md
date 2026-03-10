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
- [ ] **Description :** Texte dynamique présentant les stats (X étudiants, âge de A à B, dans C pays) calculées à partir des données.
- [x] **Graphique :** Diagramme à barres des 5 réseaux sociaux les plus utilisés (tri décroissant).

### Page 2 : Corpus (Rapport Dynamique)
Affichage de toutes les colonnes (titres en français), trié par score d'addiction.
- [x] **État principal :** Tri addiction croissant, toutes les lignes sur une page.
- [x] **Thème "Réussite" :** Surlignage vert (étudiants sans influence négative sur les résultats), tri par ID.
- [x] **Thème "Diplôme" :** Camembert représentant le nombre d'étudiants par catégorie.
- [x] **Thème "Lien Addiction-Sommeil" :** Temps de sommeil moyen par degré d'addiction.
- [ ] **Rapport personnalisé :** Un rapport au choix (justifié par sa pertinence).

### Page 3 : Exploration
- [x] Rapport avec **facettes** (Faceted Search).
- [ ] Possibilité de recherche sur tous les attributs de la table.

### Page 4 : Tableau de bord (Visualisations)
Au moins 5 graphiques pertinents pour représenter le corpus :
- [x] Répartition Homme/Femme.
- [ ] Niveaux académiques.
- [ ] Pays d'origines.
- [ ] Heures passées sur les réseaux.
- [ ] Répartition des plateformes.

### Page 5 : Résultats scolaires
- [ ] **Graphique dédié :** Nombre d'heures passées sur les réseaux en fonction du taux d'addiction.
- [ ] **Contrainte :** Titres obligatoires pour tous les axes (abscisses et ordonnées).

![[Pasted image 20260224173327.png]]
