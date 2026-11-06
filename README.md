<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/2567c080-3dea-4007-b8da-274b7757d18a" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/28dbfa70-281e-4b1d-bdae-539fb2bed145" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/85499e98-9058-4d66-af34-049a9cd79b95" />
# TP : Les attributs et méthodes statiques en C++

## Présentation

Ce TP a pour objectif de maîtriser l'utilisation des attributs et des méthodes statiques en C++ à travers trois exercices pratiques.

Les exercices permettent de comprendre comment partager des données entre plusieurs objets d'une même classe et comment gérer un état global.

## Objectifs pédagogiques

- Comprendre la notion d'attribut statique (`static`).
- Déclarer et initialiser un attribut statique.
- Utiliser une méthode statique.
- Comprendre la différence entre constructeur et destructeur.
- Manipuler un compteur partagé entre plusieurs objets.
- Appliquer les notions de programmation orientée objet en C++.

---

## Exercice 1 : Compteur d'objets

### Objectif

Utiliser un attribut statique pour compter le nombre d'objets créés à partir d'une classe.

### Description

Créer une classe `Boite` représentant une boîte avec trois attributs :

- `longueur` : longueur de la boîte.
- `largeur` : largeur de la boîte.
- `hauteur` : hauteur de la boîte.

La classe contient également un attribut statique privé `nbBoites` qui permet de compter le nombre de boîtes actuellement existantes.

### Fonctionnalités réalisées

- Déclaration de l'attribut statique `nbBoites`.
- Initialisation du compteur à zéro.
- Incrémentation du compteur dans le constructeur.
- Décrémentation du compteur dans le destructeur.
- Création de la méthode statique `getNombreBoites()`.
- Création de plusieurs objets dans la fonction `main()`.
- Affichage du nombre total de boîtes.

### Fichiers

- `Boite.h` : déclaration de la classe.
- `Boite.cpp` : implémentation des méthodes.
- `main.cpp` : création et test des objets.

### Résultat attendu

Le programme affiche le nombre de boîtes créées. Lorsque les objets sont détruits, le compteur diminue automatiquement.

---

## Exercice 2 : Taux de TVA partagé

### Objectif

Utiliser un attribut statique partagé pour appliquer un taux de TVA commun à plusieurs produits.

### Description

Créer une classe `Produit` contenant :

- `nom` : nom du produit.
- `prixHT` : prix hors taxe.
- `tauxTVA` : attribut statique représentant le taux de TVA commun à tous les produits.

Le taux initial de TVA est fixé à 20 %.

### Fonctionnalités réalisées

- Déclaration de l'attribut statique `tauxTVA`.
- Initialisation du taux à 20 %.
- Création de la méthode `getPrixTTC()` pour calculer le prix toutes taxes comprises.
- Création de la méthode statique `modifierTVA(float nouveauTaux)`.
- Modification du taux de TVA pour tous les produits.
- Affichage des prix TTC avant et après la modification du taux.

### Formule utilisée

Prix TTC = Prix HT × (1 + TVA / 100)

### Fichiers

- `Produit.h` : déclaration de la classe.
- `Produit.cpp` : implémentation des méthodes.
- `main.cpp` : création des produits et test du changement de TVA.

### Résultat attendu

Le programme affiche les prix TTC de plusieurs produits avec une TVA de 20 %, puis modifie le taux à 10 % et affiche les nouveaux prix.

La modification du taux est automatiquement appliquée à tous les produits.

---

## Exercice 3 : Gestion des sessions utilisateurs

### Objectif

Utiliser les attributs et les méthodes statiques pour gérer le nombre d'utilisateurs connectés à un système.

### Description

Créer une classe `Utilisateur` contenant :

- `nom` : nom de l'utilisateur.
- `role` : rôle de l'utilisateur (admin ou visiteur).
- `nbUtilisateursConnectes` : attribut statique privé qui compte le nombre d'utilisateurs actuellement connectés.

### Fonctionnalités réalisées

- Déclaration de l'attribut statique privé `nbUtilisateursConnectes`.
- Initialisation du compteur à zéro.
- Incrémentation du compteur dans le constructeur lors d'une connexion.
- Décrémentation du compteur dans le destructeur lors d'une déconnexion.
- Création de la méthode statique `getNbUtilisateursConnectes()`.
- Simulation de plusieurs connexions et déconnexions.
- Affichage du nombre d'utilisateurs connectés après chaque opération.

### Fichiers

- `Utilisateur.h` : déclaration de la classe.
- `Utilisateur.cpp` : implémentation des méthodes.
- `main.cpp` : simulation des connexions et déconnexions.

### Résultat attendu

Le programme affiche le nombre d'utilisateurs connectés après chaque connexion et déconnexion.

La destruction d'un objet `Utilisateur` entraîne automatiquement la diminution du compteur.

---

## Conclusion générale

À travers ces trois exercices, nous avons appris à utiliser les attributs et les méthodes statiques en C++.

Nous avons constaté qu'un attribut statique est partagé par tous les objets d'une même classe et qu'une méthode statique permet d'accéder à cet attribut sans créer d'objet.

Nous avons également appris à utiliser les constructeurs et les destructeurs pour gérer automatiquement les compteurs.

Ces exercices permettent de mieux comprendre la programmation orientée objet et la gestion des données partagées en C++.

## Technologies utilisées

- **Langage :** C++
- **IDE :** Eclipse
- **Concepts :** Programmation orientée objet, attributs statiques, méthodes statiques, constructeurs et destructeurs.
