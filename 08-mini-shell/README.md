# Projet 08 - Mini-shell

## Objectif du projet

Ecrire un mini-shell : un programme qui affiche une invite, lit une commande utilisateur, l'analyse, puis l'exécute. C'est le projet système final de cette roadmap.

Ce projet te fait découvrir la programmation système, les processus, le parsing simple, et les différences entre Linux/WSL et Windows.

## Notions de C travaillées

- boucle interactive
- lecture de ligne avec `fgets`
- découpage de chaîne en arguments
- appels système
- processus
- gestion des erreurs
- variables d'environnement
- différence entre commandes internes et programmes externes

## Enoncé

Le programme affiche une invite, par exemple `mini-shell> `. L'utilisateur tape une commande. Le shell l'exécute, affiche éventuellement le résultat, puis attend la commande suivante.

Commandes minimales attendues :

- `exit` : quitter le shell ;
- `cd` : changer de répertoire ;
- exécution d'une commande externe simple comme `ls`, `dir`, `echo`, `mkdir`.

Sous Linux ou WSL, l'exécution peut utiliser `fork`, `execvp` et `wait`. Sous Windows natif, elle peut utiliser `CreateProcess` ou une solution explicitement adaptée à Windows.

## Contraintes techniques

- Le shell doit tourner en boucle jusqu'à `exit`.
- Une ligne vide ne doit pas faire crasher le programme.
- Les arguments doivent être séparés proprement.
- Les erreurs doivent être affichées clairement.
- `cd` doit être traité comme une commande interne.
- Le projet doit préciser s'il cible Linux/WSL ou Windows natif.

## Etapes conseillées

1. Afficher une invite en boucle.
2. Lire une ligne avec `fgets`.
3. Supprimer le retour ligne final.
4. Détecter la commande `exit`.
5. Découper la ligne en commande et arguments.
6. Ajouter `cd`.
7. Exécuter une commande externe.
8. Attendre la fin du processus lancé.
9. Gérer les erreurs.
10. Ajouter un historique simple si souhaité.

## Cas de test à vérifier

- Ligne vide.
- Commande `exit`.
- Commande inconnue.
- Commande simple sans argument.
- Commande avec plusieurs arguments.
- Changement de répertoire valide.
- Changement de répertoire invalide.
- Plusieurs commandes lancées à la suite.

## Bonus

- Ajouter un prompt qui affiche le dossier courant.
- Ajouter un historique des commandes.
- Ajouter le support des guillemets simples.
- Ajouter la redirection de sortie `>`.
- Ajouter les pipes `|`.
- Ajouter des variables d'environnement simples.

## Critères de validation

- Le shell reste actif après une commande réussie.
- Le shell reste actif après une erreur.
- `exit` quitte proprement.
- Les commandes externes sont réellement exécutées.
- `cd` modifie le répertoire du shell courant.
- Le choix Linux/WSL ou Windows est clair dans le README ou les commentaires.

## Pièges classiques

- Traiter `cd` comme une commande externe alors qu'elle doit modifier le processus courant.
- Oublier d'attendre le processus enfant sous Linux.
- Découper les arguments trop naïvement sans gérer les espaces multiples.
- Ne pas gérer `fgets` qui retourne `NULL`.
- Ecrire une version dépendante de Linux puis essayer de la compiler telle quelle sous Windows.

## Ce que tu dois savoir expliquer à l'oral

- Ce qu'est un processus.
- Pourquoi un shell est principalement une boucle de lecture et d'exécution.
- La différence entre commande interne et commande externe.
- Le rôle de `fork`, `execvp` et `wait` sous Linux/WSL.
- Pourquoi Windows demande une approche différente avec `CreateProcess`.
