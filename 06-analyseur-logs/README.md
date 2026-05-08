# Projet 06 - Analyseur de logs

## Objectif du projet

Ecrire un programme qui lit un fichier texte potentiellement volumineux et produit des statistiques : nombre de lignes, nombre de mots, fréquence des lettres, mot le plus long, et éventuellement informations sur des motifs précis.

Ce projet te fait travailler la lecture de fichiers, les buffers, l'allocation dynamique et la robustesse sur de grandes entrées.

## Notions de C travaillées

- lecture de fichiers avec `fopen`, `fgets`, `fgetc`
- buffers
- allocation dynamique avec `malloc`, `realloc`, `free`
- parcours de caractères
- statistiques simples
- gestion d'erreurs
- complexité linéaire

## Enoncé

Le programme reçoit le chemin d'un fichier texte. Il lit le fichier et affiche au minimum :

- le nombre de lignes ;
- le nombre de caractères ;
- le nombre de mots ;
- la fréquence de chaque lettre ;
- le mot le plus long.

Le programme doit gérer un fichier trop grand pour être chargé entièrement en mémoire dans une première version simple.

## Contraintes techniques

- Le chemin du fichier peut être demandé à l'utilisateur ou passé en argument.
- Le programme doit refuser proprement un fichier introuvable.
- La lecture doit se faire progressivement.
- Toute mémoire allouée dynamiquement doit être libérée.
- Les majuscules et minuscules doivent être traitées de manière cohérente.
- Les caractères non alphabétiques ne doivent pas fausser la fréquence des lettres.

## Etapes conseillées

1. Ouvrir un fichier et vérifier que l'ouverture réussit.
2. Compter les lignes avec `fgets`.
3. Compter les caractères.
4. Détecter les mots avec un état `inside_word`.
5. Compter les lettres de `a` à `z`.
6. Stocker le mot le plus long.
7. Ajouter de l'allocation dynamique pour gérer un mot long.
8. Nettoyer toutes les ressources avant la fin du programme.

## Cas de test à vérifier

- Fichier vide.
- Fichier d'une seule ligne.
- Fichier avec plusieurs lignes.
- Fichier contenant seulement des espaces.
- Fichier avec ponctuation.
- Fichier avec majuscules et minuscules.
- Fichier introuvable.
- Fichier contenant un mot très long.

## Bonus

- Afficher les 10 mots les plus fréquents.
- Lire le chemin du fichier depuis `argv`.
- Générer un rapport dans un fichier de sortie.
- Supporter des fichiers CSV simples.
- Ajouter une option pour ignorer ou inclure la casse.
- Mesurer le temps d'exécution.

## Critères de validation

- Le programme affiche des statistiques cohérentes.
- Un fichier absent produit une erreur claire.
- Le programme ne charge pas inutilement tout le fichier en mémoire.
- La mémoire dynamique est libérée.
- Les tests couvrent les fichiers vides et les entrées inhabituelles.

## Pièges classiques

- Oublier de compter la dernière ligne si elle ne finit pas par un retour ligne.
- Confondre caractères, octets et lettres.
- Ne pas libérer une zone allouée après `realloc`.
- Lire au-delà de la fin d'un buffer.
- Compter plusieurs espaces comme plusieurs mots vides.

## Ce que tu dois savoir expliquer à l'oral

- Pourquoi lire progressivement un gros fichier.
- Comment tu détectes le début et la fin d'un mot.
- Quand utiliser `malloc` et quand utiliser un tableau fixe.
- Pourquoi chaque `malloc` doit avoir un `free`.
- Comment tu testerais les fuites mémoire.
