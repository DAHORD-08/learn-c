# Roadmap C - Apprendre par projets

Cette roadmap a pour objectif de te faire apprendre le langage C en réalisant des projets concrets, avec une difficulté qui monte progressivement. L'idée n'est pas seulement d'obtenir un programme qui marche, mais de comprendre ce que tu écris, de savoir le tester, et de pouvoir expliquer tes choix comme dans un contexte d'école d'ingénieur.

Chaque projet doit être traité comme un vrai exercice technique : lecture du sujet, découpage du problème, implémentation progressive, tests, correction des warnings, puis explication orale des notions utilisées.

## Progression conseillée

1. [Mastermind terminal](01-mastermind-terminal/README.md)
2. [Convertisseur de bases](02-convertisseur-bases/README.md)
3. [Mini string.h](03-mini-string-h/README.md)
4. [Validateur Sudoku](04-validateur-sudoku/README.md)
5. [Gestionnaire de contacts](05-gestionnaire-contacts/README.md)
6. [Analyseur de logs](06-analyseur-logs/README.md)
7. [Sudoku solver](07-sudoku-solver/README.md)
8. [Mini-shell](08-mini-shell/README.md)

## Niveaux de progression

### Niveau 1 - Fondations

Tu apprends à écrire un programme simple, à manipuler des variables, à utiliser des conditions, des boucles, et à lire des entrées utilisateur. L'objectif est de devenir à l'aise avec le cycle de base : écrire, compiler, exécuter, corriger.

Projets concernés :

- Mastermind terminal
- Convertisseur de bases

### Niveau 2 - Tableaux, chaînes et pointeurs

Tu passes de petits programmes linéaires à des programmes qui manipulent des collections de données. C'est aussi le moment de comprendre les chaînes C, le caractère nul `'\0'`, les adresses mémoire, et les pointeurs.

Projets concernés :

- Mini string.h
- Validateur Sudoku

### Niveau 3 - Structures et fichiers

Tu apprends à organiser des données plus riches avec `struct`, puis à les conserver entre deux exécutions grâce aux fichiers. Le programme commence à ressembler à une petite application.

Projet concerné :

- Gestionnaire de contacts

### Niveau 4 - Allocation dynamique

Tu apprends à demander de la mémoire au système avec `malloc`, à la libérer avec `free`, et à raisonner sur la durée de vie des données. C'est une étape centrale du C.

Projet concerné :

- Analyseur de logs

### Niveau 5 - Algorithmes avancés

Tu utilises la récursivité et le backtracking pour résoudre un problème combinatoire. Le but est de comprendre comment explorer des possibilités, revenir en arrière, et garantir qu'une solution respecte des contraintes.

Projet concerné :

- Sudoku solver

### Niveau 6 - Programmation système

Tu construis un programme qui interagit avec le système d'exploitation. Tu découvres la boucle d'un shell, le parsing de commandes, la création de processus, et les différences entre Linux/WSL et Windows.

Projet concerné :

- Mini-shell

## Règles générales de travail

- Compile souvent, idéalement après chaque petite étape.
- Active les warnings stricts : `-Wall -Wextra -Werror` quand c'est possible.
- Lis les erreurs du compilateur au lieu de les contourner.
- Teste les entrées invalides : texte au lieu d'un nombre, valeurs hors limites, fichiers absents, lignes vides.
- Evite le copier-coller aveugle : tu dois pouvoir expliquer chaque ligne importante.
- Documente les choix non évidents dans le code ou dans un court fichier de notes.
- Garde des programmes simples au début, puis structure davantage quand le projet grossit.

## Evolution technique attendue

- Projets 1 et 2 : un seul fichier `.c` est acceptable.
- Projets 3 et 4 : commence à séparer les fonctions proprement.
- A partir du projet 5 : utilise plusieurs fichiers `.c` / `.h`.
- A partir du projet 5 : ajoute un `Makefile`.
- A partir du projet 6 : surveille les fuites mémoire avec Valgrind si tu travailles sous Linux ou WSL.
- A partir du projet 7 : écris des tests ciblés pour les fonctions critiques.

## Critère global de réussite

Un projet est vraiment terminé si :

- il compile sans warning important ;
- il ne crash pas sur les cas simples d'erreur ;
- il respecte l'énoncé ;
- il est lisible par quelqu'un d'autre ;
- tu sais expliquer les notions de C utilisées ;
- tu sais montrer au moins cinq tests pertinents.
