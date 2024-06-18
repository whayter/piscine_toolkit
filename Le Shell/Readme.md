# Le Shell

Le Shell est un environnement d'interprétation de commandes utilisé principalement dans les systèmes Unix et Unix-like (comme Linux et macOS). C'est l'interface entre l'utilisateur et le système d'exploitation, permettant d'exécuter des commandes, de lancer des programmes et d'automatiser des tâches via des scripts.

Le Shell offre une interface en ligne de commande où les utilisateurs peuvent taper des commandes pour interagir avec le système d'exploitation. Cette interface est accessible via un terminal.

Il est également possible d'écrired des scripts Shell pour automatiser des tâches répétitives. Ces scripts peuvent contenir des commandes, des boucles, des conditions et des fonctions.



## Pour commencer



Il suffit d'ouvrir un terminal

Faire le point sur la notion de répertoire, répertoire courant, fichier caché, etc




## Les principales commandes Shell


Point général sur les commandes, les options, comment ça s'utilise et tout


### I. Naviguer dans le système de fichiers

#### 1. Lister les fichiers et dossiers

La commande `ls` (pour *list*) permet de lister les fichiers et dossiers dans le répertoire courant. 

L'option `-l` permet d'obtenir affichage détaillé (permissions, propriétaire, taille, date de modification).

L'option `-a` permet d'afficher tous les fichiers, y compris les fichiers cachés (ceux dont le nom commence par un point).

L'option `-R` permet un affichage récursif des sous-répertoires.

#### 2. Naviguer entre les répertoires

La commande `cd`(pour *change directory*) permet de changer de répertoire : `cd [répertoire]`.

Il existe quelques raccourcis très pratiques :
* `~` permet d'accéder au répertoire utilisateur (home) : `cd ~`
* `..` permet d'accéder au répertoire parent : `cd ..`
* `-` permet d'accéder au répertoire précédent : `cd -`

#### 3. Afficher le chemin absolu du répertoire courant

La commande `pwd` (pour *print working directory*) permet d'afficher le chemin absolu du répertoire dans lequel on se trouve.



### II. Manipuler les fichiers et répertoires

#### 1. Copier des fichiers ou des répertoires

La commande `cp` (pour *copy*) permet de copier des fichiers ou des répertoires d'un emplacement à un autre : `cp [source] [destination]`.

#### 2. Déplacer ou renommer des fichiers ou des répertoires

La commande `mv` (pour *move*) permet de déplacer des fichiers ou des répertoires d'un emplacement à un autre : `mv [source] [destination]`.

Il est aussi possible de déplacer plusieures sources à la fois : `mv [source1] [source2] [destination]`.

Cette commande est également utilisée pour renommer un fichier ou un répertoire : `mv [ancien nom de fichier] [nouveau nom de fichier]`.

#### 3. Supprimer un fichier ou un répertoire

La commande `rm` (pour *remove*) permet de supprimer un fichier spécifié : `rm [fichier]`. Il est également possible de supprimer plusieurs fichiers à la fois : `rm [fichier1] [fichier2] [fichier3]`.

Pour supprimer un répertoire vide, il faut utiliser l'option `-d` (pour *directory*). Sinon, on peut supprimer un répertoire non vide grâce à l'option `-r` (pour *recursive*) : `rm -r [répertoire]`. 

Il convient d'être prudent avec cette commande, les erreurs arrivent vite et peuvent être fatales. L'option `-i` permet d'ajouter une confirmation avant de supprimer chaque fichier spécifié. 

#### 4. Créer un répertoire

La commande `mkdir` (pour *make directory*) permet de créer un nouveau répertoire et s'utilise de cette façon : `mkdir [répertoire]`.


### III. Affichage

#### 1. Afficher un message

La commande `echo` permet d'afficher un message dans la console : `echo "Hello, world!"`.

#### 2. Afficher le contenu d'un fichier

La commande `cat` permet d'afficher dans la console le contenu d'un fichier spécifié : `cat [fichier]`.

#### 3. Afficher les premières lignes d'un fichier

La commande `head` permet d'afficher dans la console les 10 premières lignes d'un fichier spécifié : `head [fichier]`. Il est possible de modifier le nombre de lignes à afficher avec l'option `-n`: `head -n 20 [fichier]`. Dans ce dernier exemple, on affichera les 20 premières lignes du fichier. 

#### 4. Afficher les denières lignes d'un fichier

La commande `tail` permet d'afficher dans la console les 10 denières lignes d'un fichier spécifié : `tail [fichier]`. Il est possible de modifier le nombre de lignes à afficher avec l'option `-n`: `tail -n 20 [fichier]`. Dans ce dernier exemple, on affichera les 20 denières lignes du fichier. 




### IV. Redirections

#### 1. Rediriger la sortie d'une commande vers un fichier

Le symbole `>` permet de rediriger la sortie d'une commande vers un fichier : `[command] > [fichier]`.

#### 2. Ajouter la sortie d'une commande à la fin d'un fichier

Le symbole `>>` permet d'ajouter la sortie d'une commande à la fin d'un fichier : `[command] >> [fichier]`.

#### 3. Rediriger la sortie d'une commande vers l'entrée d'une autre commande

Il est possible de chaîner des commandes grâce au symbole `|`(appelé *pipe*), permettant ainsi d'utiliser la sortie d'une commande comme entrée d'une autre commande : `[command1] | [command2]`.

Concrètement, s
* `[command1] | [command2]` permet d'utiliser la sortie de command1 comme entrée pour command2.


### V. Documentation

`man [command]` permet d'afficher le manuel d'utilisation de la commande spécifiée. Par exemple, `man echo` donnera toutes les informations nécessaires pour utiliser la commande `echo` à son plein potentiel. C'est une véritable bible et un compagnon de route infaillible. 

Tu verras probablement passer le sigle *RTFM*, qui signifie *Read The Fucking Man*. Si tu as une question, commence toujours par lire le man !
