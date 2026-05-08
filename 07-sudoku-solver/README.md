# Projet 07 - Sudoku solver

## Objectif du projet

Transformer le validateur Sudoku en solveur capable de remplir une grille incomplète. Le programme doit trouver une solution valide en utilisant la récursivité et le backtracking.

Ce projet est une introduction sérieuse aux algorithmes de recherche et au raisonnement récursif.

## Notions de C travaillées

- récursivité
- backtracking
- tableaux 2D
- réutilisation de fonctions de validation
- recherche exhaustive contrôlée
- conditions d'arrêt
- séparation entre résolution et affichage

## Enoncé

Le programme reçoit une grille de Sudoku incomplète, avec `0` pour les cases vides. Il tente de compléter la grille de manière à respecter toutes les règles du Sudoku. Si une solution existe, il l'affiche. Sinon, il indique qu'aucune solution n'a été trouvée.

## Contraintes techniques

- Réutiliser les fonctions de validation du projet précédent.
- Ne jamais placer un chiffre qui viole les règles.
- Utiliser une fonction récursive de résolution.
- Laisser la grille dans un état cohérent après un échec.
- Gérer le cas d'une grille déjà complète.
- Gérer le cas d'une grille invalide dès le départ.

## Etapes conseillées

1. Reprendre le validateur Sudoku.
2. Ecrire une fonction qui trouve la prochaine case vide.
3. Ecrire une fonction qui teste si un chiffre peut être placé.
4. Placer un chiffre candidat.
5. Appeler récursivement le solveur.
6. Annuler le placement si la suite échoue.
7. Afficher la grille résolue.
8. Ajouter la lecture depuis un fichier.

## Cas de test à vérifier

- Grille déjà résolue.
- Grille simple avec une seule case vide.
- Grille classique avec une solution.
- Grille invalide dès le départ.
- Grille sans solution.
- Grille vide.

## Bonus

- Compter le nombre de solutions.
- Arrêter après deux solutions pour détecter une grille ambiguë.
- Ajouter une heuristique : choisir la case avec le moins de candidats.
- Mesurer le nombre d'appels récursifs.
- Afficher les étapes de résolution en mode debug.

## Critères de validation

- Le solveur trouve une solution valide quand elle existe.
- Le programme annonce clairement l'absence de solution.
- Les règles du Sudoku ne sont jamais contournées.
- La récursivité a une condition d'arrêt claire.
- Le code de validation reste séparé du code de résolution.

## Pièges classiques

- Oublier d'annuler une valeur après un échec récursif.
- Accepter une grille invalide avant même la résolution.
- Croire qu'une fonction récursive doit toujours retourner `void`.
- Modifier la grille de manière irréversible.
- Résoudre par hasard sans vérifier les blocs 3x3.

## Ce que tu dois savoir expliquer à l'oral

- Ce qu'est le backtracking.
- Pourquoi la récursivité convient au Sudoku.
- Quelle est la condition d'arrêt du solveur.
- Pourquoi il faut annuler un choix quand il mène à une impasse.
- Comment tu détectes qu'une grille n'a pas de solution.
