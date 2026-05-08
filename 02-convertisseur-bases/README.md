# Projet 02 - Convertisseur de bases

## Objectif du projet

Ecrire un programme qui convertit un nombre décimal vers une autre base, d'abord en binaire et en hexadécimal, puis éventuellement vers d'autres bases.

Ce projet te fait manipuler les divisions successives, le modulo, les tableaux, et la représentation des nombres en mémoire.

## Notions de C travaillées

- types numériques : `int`, `unsigned int`, `long`
- opérateur modulo `%`
- division entière
- tableaux de caractères
- boucles
- fonctions de conversion
- affichage formaté

## Enoncé

Le programme demande à l'utilisateur un nombre entier positif en base 10, puis lui propose une base de sortie : binaire, octal, décimal ou hexadécimal. Il affiche ensuite le résultat converti.

La conversion doit être réalisée par ton propre algorithme. Pour la version principale, n'utilise pas directement `%x` ou `%o` pour faire tout le travail.

## Contraintes techniques

- Le nombre saisi doit être positif ou nul.
- Le programme doit gérer le cas particulier `0`.
- Le résultat doit être stocké avant affichage, car les divisions successives produisent les chiffres dans l'ordre inverse.
- Les chiffres hexadécimaux doivent utiliser `A`, `B`, `C`, `D`, `E`, `F`.
- Le programme doit refuser une base non supportée.

## Etapes conseillées

1. Lire un entier décimal.
2. Convertir uniquement vers le binaire.
3. Stocker les restes dans un tableau.
4. Afficher le tableau dans l'ordre inverse.
5. Généraliser vers une fonction `convert_base(number, base)`.
6. Ajouter le support de l'hexadécimal.
7. Ajouter un menu de choix de base.
8. Tester les limites des types utilisés.

## Cas de test à vérifier

- `0` en binaire donne `0`.
- `1` en binaire donne `1`.
- `10` en binaire donne `1010`.
- `255` en hexadécimal donne `FF`.
- `16` en hexadécimal donne `10`.
- Une base interdite est rejetée.
- Une entrée négative est rejetée.

## Bonus

- Convertir depuis n'importe quelle base vers n'importe quelle autre base.
- Supporter les bases de 2 à 16.
- Afficher aussi la représentation avec les préfixes `0b`, `0o`, `0x`.
- Comparer ton résultat avec `printf("%x")` pour vérifier.
- Supporter des nombres plus grands avec `unsigned long long`.

## Critères de validation

- Les conversions sont correctes pour les cas simples.
- Le cas `0` est traité explicitement.
- Le programme n'utilise pas les formats de `printf` comme solution principale.
- Les erreurs de saisie sont gérées.
- La logique de conversion est isolée dans une ou plusieurs fonctions.

## Pièges classiques

- Afficher les restes dans le mauvais ordre.
- Oublier que la division entière tronque le résultat.
- Déborder du tableau si le nombre est grand.
- Confondre la valeur numérique `10` avec le caractère `'A'`.

## Ce que tu dois savoir expliquer à l'oral

- Pourquoi le modulo donne le chiffre de droite dans la base cible.
- Pourquoi il faut inverser l'ordre des restes.
- La différence entre un entier et sa représentation textuelle.
- Pourquoi `255` vaut `FF` en hexadécimal.
- Les limites du type numérique que tu utilises.
