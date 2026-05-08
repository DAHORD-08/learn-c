# Projet 04 - Validateur Sudoku

## Objectif du projet

Ecrire un programme qui vérifie si une grille de Sudoku est valide. Le programme ne résout pas encore la grille : il vérifie seulement que les règles ne sont pas violées.

Ce projet te fait travailler les tableaux à deux dimensions, les boucles imbriquées, et la validation de contraintes.

## Notions de C travaillées

- tableaux 2D : `int grid[9][9]`
- boucles imbriquées
- fonctions de validation
- constantes symboliques
- découpage en sous-problèmes
- représentation d'une grille

## Enoncé

Une grille de Sudoku contient 9 lignes, 9 colonnes et 9 blocs de taille 3x3. Chaque ligne, colonne et bloc doit contenir au plus une fois chaque chiffre de 1 à 9. Une case vide peut être représentée par `0`.

Le programme doit lire ou contenir une grille, puis indiquer si elle est valide.

## Contraintes techniques

- La grille doit avoir exactement 9 lignes et 9 colonnes.
- Les valeurs autorisées sont de `0` à `9`.
- Une valeur `0` représente une case vide.
- Une ligne ne doit pas contenir deux fois le même chiffre non nul.
- Même règle pour les colonnes et les blocs 3x3.
- Le programme doit afficher clairement où se trouve l'erreur si possible.

## Etapes conseillées

1. Déclarer une grille fixe dans le code.
2. Ecrire une fonction qui valide une ligne.
3. Ecrire une fonction qui valide une colonne.
4. Ecrire une fonction qui valide un bloc 3x3.
5. Ecrire une fonction globale `is_valid_grid`.
6. Ajouter l'affichage de la grille.
7. Ajouter la lecture d'une grille depuis le terminal ou un fichier.

## Cas de test à vérifier

- Grille vide remplie de `0` : valide.
- Ligne contenant deux fois `5` : invalide.
- Colonne contenant deux fois `7` : invalide.
- Bloc 3x3 contenant deux fois `9` : invalide.
- Grille contenant une valeur `12` : invalide.
- Grille complète correcte : valide.

## Bonus

- Lire une grille depuis un fichier texte.
- Afficher les coordonnées exactes des conflits.
- Permettre une saisie interactive ligne par ligne.
- Ajouter une fonction qui vérifie si une grille complète est entièrement résolue.
- Préparer les fonctions pour le futur Sudoku solver.

## Critères de validation

- Les lignes, colonnes et blocs sont tous vérifiés.
- Les cases vides sont acceptées.
- Les valeurs hors limites sont refusées.
- Le code ne duplique pas inutilement la même logique partout.
- Les fonctions sont petites et testables.

## Pièges classiques

- Vérifier seulement les lignes et oublier les blocs.
- Traiter `0` comme un chiffre normal et le compter comme doublon.
- Se tromper dans le calcul du début d'un bloc 3x3.
- Inverser ligne et colonne dans les indices.
- Cacher les erreurs en renvoyant seulement `true` ou `false` sans diagnostic.

## Ce que tu dois savoir expliquer à l'oral

- Comment un tableau 2D est indexé.
- Comment tu parcours une ligne, une colonne et un bloc.
- Pourquoi `0` doit être ignoré dans la détection de doublons.
- Comment calculer le bloc 3x3 d'une case.
- Comment tu éviterais de répéter trop de code.
