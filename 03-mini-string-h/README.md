# Projet 03 - Mini string.h

## Objectif du projet

Recréer une petite partie de la bibliothèque `string.h` pour comprendre comment les chaînes de caractères fonctionnent réellement en C.

Ce projet est central : il te force à comprendre les tableaux de `char`, le caractère nul `'\0'`, les pointeurs, et le passage de chaînes à des fonctions.

## Notions de C travaillées

- chaînes de caractères C
- tableaux de `char`
- caractère de fin `'\0'`
- pointeurs `char *`
- parcours mémoire
- fonctions qui reçoivent et retournent des pointeurs
- comparaison caractère par caractère

## Enoncé

Tu dois écrire ta propre mini-bibliothèque de manipulation de chaînes. Elle devra contenir plusieurs fonctions inspirées de `string.h`, puis un petit programme de démonstration qui les appelle.

Fonctions minimales attendues :

- `my_strlen` : calculer la longueur d'une chaîne.
- `my_strcpy` : copier une chaîne dans un autre tableau.
- `my_strcmp` : comparer deux chaînes.
- `my_strrev` : inverser une chaîne en place.
- `my_count_words` : compter les mots d'une phrase simple.

## Contraintes techniques

- Ne pas appeler les fonctions équivalentes de `string.h` pour implémenter les tiennes.
- Les fonctions doivent s'arrêter au caractère `'\0'`.
- Les fonctions doivent être testées avec des chaînes vides.
- `my_strrev` doit modifier la chaîne reçue, pas seulement afficher l'inverse.
- Pour commencer, un mot peut être défini comme une suite de caractères séparée par des espaces.

## Etapes conseillées

1. Ecrire `my_strlen` avec un indice de tableau.
2. Réécrire `my_strlen` avec un pointeur.
3. Ecrire `my_strcpy`.
4. Ecrire `my_strcmp`.
5. Ecrire `my_strrev`.
6. Ecrire `my_count_words`.
7. Créer un petit programme qui teste chaque fonction.
8. Séparer la bibliothèque dans un fichier `.c` et un fichier `.h`.

## Cas de test à vérifier

- Longueur de `"abc"` : `3`.
- Longueur de `""` : `0`.
- Copie de `"hello"` dans un tableau assez grand.
- Comparaison de deux chaînes identiques.
- Comparaison de `"abc"` et `"abd"`.
- Inversion de `"abcd"` : `"dcba"`.
- Comptage des mots dans `"bonjour le monde"` : `3`.
- Comptage des mots dans une chaîne vide.

## Bonus

- Ajouter `my_strcat`.
- Ajouter `my_strchr`.
- Ajouter `my_strdup` avec allocation dynamique.
- Gérer les tabulations et retours à la ligne dans `my_count_words`.
- Créer un mini programme de test automatique.

## Critères de validation

- Les fonctions donnent les mêmes résultats que les fonctions standard pour les cas simples.
- Les chaînes vides sont gérées.
- Les fonctions ne lisent pas au-delà du `'\0'`.
- Le code est séparé en `.c` et `.h` si tu es à l'aise.
- Tu peux expliquer chaque manipulation de pointeur.

## Pièges classiques

- Oublier de copier le `'\0'` dans `my_strcpy`.
- Utiliser un pointeur non initialisé.
- Ecrire dans une chaîne littérale avec `my_strrev`.
- Confondre `char *s` et `char s[]` sans comprendre le contexte.
- Lire une case après la fin de la chaîne.

## Ce que tu dois savoir expliquer à l'oral

- Ce qu'est une chaîne de caractères en C.
- Le rôle exact du caractère `'\0'`.
- La différence entre parcourir avec un indice et parcourir avec un pointeur.
- Pourquoi `my_strcpy` suppose que la destination est assez grande.
- Pourquoi modifier une chaîne littérale est dangereux.
