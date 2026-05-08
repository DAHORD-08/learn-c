# Projet 01 - Mastermind terminal

## Objectif du projet

Ecrire un jeu de Mastermind en terminal. L'ordinateur choisit un nombre secret de 4 chiffres, et le joueur doit le deviner. Après chaque tentative, le programme indique combien de chiffres sont bien placés et combien sont présents mais mal placés.

Ce projet sert à prendre confiance avec la syntaxe C, les variables, les conditions, les boucles, et les entrées/sorties.

## Notions de C travaillées

- `printf` et `scanf`
- variables de type `int`
- conditions `if`, `else if`, `else`
- boucles `while` ou `for`
- opérateurs arithmétiques
- génération pseudo-aléatoire avec `rand`
- découpage d'un nombre en chiffres
- validation simple d'une saisie utilisateur

## Enoncé

Le programme génère un code secret composé de 4 chiffres. Le joueur entre une proposition de 4 chiffres. Le programme compare la proposition au code secret et affiche :

- le nombre de chiffres corrects et bien placés ;
- le nombre de chiffres corrects mais mal placés.

La partie continue jusqu'à ce que le joueur trouve le code ou atteigne un nombre maximal d'essais.

## Contraintes techniques

- Le programme doit être jouable entièrement dans le terminal.
- Le code secret doit contenir exactement 4 chiffres.
- Une proposition invalide ne doit pas faire crasher le programme.
- Le joueur doit voir son nombre d'essais restants.
- Pour une première version, tu peux accepter les chiffres répétés ou les interdire, mais ton choix doit être clair.

## Etapes conseillées

1. Afficher un message d'accueil et lire une proposition.
2. Stocker temporairement un code secret fixe, par exemple `1234`.
3. Comparer chaque position pour compter les chiffres bien placés.
4. Ajouter le comptage des chiffres présents mais mal placés.
5. Ajouter une boucle de jeu avec un nombre limité d'essais.
6. Remplacer le code fixe par un code généré aléatoirement.
7. Gérer les entrées invalides.

## Cas de test à vérifier

- Code secret `1234`, proposition `1234` : 4 bien placés, 0 mal placé.
- Code secret `1234`, proposition `4321` : 0 bien placé, 4 mal placés.
- Code secret `1234`, proposition `1567` : 1 bien placé, 0 mal placé.
- Proposition trop courte ou trop longue.
- Proposition contenant autre chose que des chiffres.
- Victoire au premier essai.
- Défaite après le dernier essai.

## Bonus

- Ajouter un mode difficile avec 6 chiffres.
- Ajouter un historique des essais.
- Permettre au joueur de choisir si les chiffres peuvent se répéter.
- Ajouter une option pour rejouer sans relancer le programme.
- Afficher une aide courte pendant la partie.

## Critères de validation

- Le jeu se termine correctement en cas de victoire ou de défaite.
- Les indices affichés sont cohérents.
- Le programme ne révèle pas le code secret pendant la partie.
- Les saisies invalides sont rejetées proprement.
- Le code est lisible et découpé en fonctions simples si possible.

## Pièges classiques

- Compter deux fois le même chiffre comme mal placé.
- Oublier de vider ou contrôler l'entrée utilisateur après un `scanf` raté.
- Générer toujours le même nombre aléatoire faute d'initialisation.
- Confondre chiffre, caractère, et nombre entier.

## Ce que tu dois savoir expliquer à l'oral

- La différence entre une boucle `while` et une boucle `for`.
- Comment tu compares deux codes chiffre par chiffre.
- Comment tu évites de compter deux fois un chiffre.
- Ce que fait `scanf` quand l'entrée ne correspond pas au format attendu.
- Pourquoi un programme doit valider les entrées utilisateur.
