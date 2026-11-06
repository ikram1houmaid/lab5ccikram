# TP : Les attributs et méthodes statiques en C++

## Présentation
Ce TP contient trois exercices pratiques en C++ permettant de comprendre et de manipuler les attributs statiques, les méthodes statiques, les constructeurs et les destructeurs.

## Objectifs
- Comprendre le fonctionnement du mot-clé `static`.
- Utiliser les attributs statiques partagés entre plusieurs objets.
- Déclarer et utiliser des méthodes statiques.
- Comprendre le rôle des constructeurs et des destructeurs.
- Gérer la création et la destruction des objets.

---

## Exercice 1 : Compteur d’objets

### Objectif
Créer une classe `Boite` représentant une boîte avec trois dimensions : longueur, largeur et hauteur.

### Travail réalisé
- Déclaration des attributs longueur, largeur et hauteur.
- Création d'un attribut statique `nbBoites` pour compter les objets créés.
- Utilisation d'un constructeur pour incrémenter le compteur.
- Utilisation d'un destructeur pour décrémenter le compteur.
- Création d'une méthode statique `getNombreBoites()` pour retourner le nombre de boîtes existantes.

### Résultat attendu
Afficher le nombre total de boîtes créées et vérifier que le compteur diminue lors de la destruction des objets.

---

## Exercice 2 : Taux de TVA partagé

### Objectif
Créer une classe `Produit` permettant de calculer le prix TTC à partir du prix HT et d'un taux de TVA commun.

### Travail réalisé
- Déclaration des attributs `nom` et `prixHT`.
- Création d'un attribut statique `tauxTVA`.
- Initialisation du taux de TVA à 20 %.
- Création de la méthode `getPrixTTC()` pour calculer le prix toutes taxes comprises.
- Création de la méthode statique `modifierTVA(float nouveauTaux)` pour modifier le taux de TVA de tous les produits.

### Formule utilisée

Prix TTC = Prix HT × (1 + TVA / 100)

### Résultat attendu
Créer plusieurs produits, afficher leurs prix TTC, modifier le taux de TVA et constater que le nouveau taux est appliqué à tous les produits.

---

## Exercice 3 : Gestion des sessions utilisateurs

### Objectif
Créer une classe `Utilisateur` permettant de gérer le nombre d'utilisateurs actuellement connectés.

### Travail réalisé
- Déclaration des attributs `nom` et `role`.
- Création d'un attribut statique privé `nbUtilisateursConnectes`.
- Utilisation du constructeur pour augmenter le nombre d'utilisateurs connectés.
- Utilisation du destructeur pour diminuer le nombre d'utilisateurs connectés.
- Création d'une méthode statique `getNbUtilisateursConnectes()` pour consulter le nombre d'utilisateurs connectés.
- Utilisation de `new` pour créer des objets et de `delete` pour les détruire.

### Résultat attendu
Simuler la connexion et la déconnexion de plusieurs utilisateurs et afficher le nombre d'utilisateurs connectés après chaque opération.

---

## Structure du projet

```text
TP_Static/
│
├── src/
│   ├── Boite.cpp
│   ├── Produit.cpp
│   └── Utilisateur.cpp
│
└── README.md
```

**Remarque :** Chaque fichier contient son propre programme `main()`. Les trois exercices doivent donc être exécutés séparément.

---

## Environnement de développement
- **Langage :** C++
- **IDE :** Eclipse
- **Compilateur :** GCC / MinGW
- **Bibliothèque utilisée :** iostream

## Conclusion
Ce TP permet de maîtriser les notions fondamentales de la programmation orientée objet en C++, notamment les attributs statiques, les méthodes statiques, les constructeurs et les destructeurs. Il montre également comment partager des données entre plusieurs objets d'une même classe.
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/b21d48e0-6f5d-49b2-862b-0921e2e348c0" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/fe8d7af0-39ed-49d6-93fb-06771ff68999" />
<img width="960" height="540" alt="image" src="https://github.com/user-attachments/assets/21de39da-79ef-4a79-8b2e-6e69321c90d4" />
