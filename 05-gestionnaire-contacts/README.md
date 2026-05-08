# Projet 05 - Gestionnaire de contacts

## Objectif du projet

Construire un carnet d'adresses en terminal capable d'ajouter, afficher, rechercher, modifier et supprimer des contacts. Les contacts doivent être sauvegardés dans un fichier pour être retrouvés au redémarrage.

Ce projet introduit une organisation plus sérieuse du code : `struct`, fichiers, menu, séparation en modules et, idéalement, `Makefile`.

## Notions de C travaillées

- `struct`
- tableaux de structures
- fonctions de manipulation de données
- fichiers texte avec `fopen`, `fprintf`, `fscanf`, `fgets`
- menu interactif
- séparation `.c` / `.h`
- constantes de taille

## Enoncé

Chaque contact contient au minimum :

- un prénom ;
- un nom ;
- un numéro de téléphone ;
- une adresse email.

Le programme affiche un menu permettant de :

- ajouter un contact ;
- lister tous les contacts ;
- rechercher un contact ;
- modifier un contact ;
- supprimer un contact ;
- sauvegarder les contacts ;
- charger les contacts depuis un fichier ;
- quitter.

## Contraintes techniques

- Utiliser une `struct Contact`.
- Stocker plusieurs contacts dans un tableau.
- Définir une capacité maximale pour la première version.
- Sauvegarder les données dans un fichier texte.
- Charger le fichier au démarrage si possible.
- Ne pas perdre les données lors d'une modification ou suppression.
- Gérer proprement les champs vides ou trop longs.

## Etapes conseillées

1. Définir la structure `Contact`.
2. Créer un menu simple en boucle.
3. Ajouter la création d'un contact.
4. Ajouter l'affichage de tous les contacts.
5. Ajouter la recherche par nom.
6. Ajouter la modification.
7. Ajouter la suppression.
8. Ajouter la sauvegarde dans un fichier.
9. Ajouter le chargement depuis le fichier.
10. Séparer le code en plusieurs fichiers.

## Cas de test à vérifier

- Ajouter un contact puis l'afficher.
- Rechercher un contact existant.
- Rechercher un contact absent.
- Modifier un numéro de téléphone.
- Supprimer le premier contact.
- Supprimer le dernier contact.
- Sauvegarder, quitter, relancer, puis recharger.
- Charger un fichier inexistant.

## Bonus

- Trier les contacts par nom.
- Ajouter une recherche insensible à la casse.
- Utiliser une allocation dynamique au lieu d'une capacité fixe.
- Sauvegarder en CSV propre.
- Ajouter un export lisible.
- Ajouter un identifiant unique par contact.

## Critères de validation

- Toutes les opérations CRUD fonctionnent.
- Les contacts persistent entre deux exécutions.
- Le programme ne crash pas si le fichier est absent.
- Les suppressions ne laissent pas de trous incohérents dans le tableau.
- Le code est organisé en modules.
- Un `Makefile` permet de compiler le projet.

## Pièges classiques

- Utiliser `scanf("%s")` et perdre les espaces dans les noms composés.
- Oublier de fermer un fichier avec `fclose`.
- Ecraser le fichier avant d'avoir validé les données.
- Mal décaler les éléments après une suppression.
- Mélanger logique métier, affichage et lecture utilisateur dans une seule grosse fonction.

## Ce que tu dois savoir expliquer à l'oral

- Pourquoi une `struct` est adaptée pour représenter un contact.
- Comment le tableau de contacts est organisé.
- Comment fonctionne la sauvegarde fichier.
- La différence entre fichier texte et fichier binaire.
- Comment tu gères la suppression d'un élément dans un tableau.
