# Le Shell

Le Shell est un environnement d'interprétation de commandes utilisé principalement dans les systèmes Unix et Unix-like (comme Linux et macOS). C'est l'interface entre l'utilisateur et le système d'exploitation, permettant d'exécuter des commandes, de lancer des programmes et d'automatiser des tâches via des scripts.

Le Shell offre une interface en ligne de commande où les utilisateurs peuvent taper des commandes pour interagir avec le système d'exploitation. Cette interface est accessible via un terminal.

Il est également possible d'écrired des scripts Shell pour automatiser des tâches répétitives. Ces scripts peuvent contenir des commandes, des boucles, des conditions et des fonctions.



## Pour commencer



Il suffit d'ouvrir un terminal

Faire le point sur la notion de répertoire, répertoire courant, fichier caché, etc




## Les principales commandes Shell




### I. Naviguer dans le système de fichiers

#### 1. lister les fichiers et dossiers

La commande `ls` permet de lister les fichiers et dossiers dans le répertoire (= dossier) courant.

#### 2. cd

`cd [nom_du_répertoire]` permet de changer de répertoire.

#### 3. pwd

`pwd` permet d'afficher le chemin du répertoire courant.







### II. Manipuler les fichiers et répertoires

#### 1. Copier des fichiers ou des répertoires

La commande `cp` permet de copier des fichiers ou des répertoires d'un emplacement à un autre : `cp [source] [destination]`.

#### 2. Déplacer des fichiers ou des répertoires

La commande `mv` permet de déplacer ou renommer des fichiers ou des répertoires d'un emplacement à un autre : `mv [source] [destination]`.

#### 3. Supprimer un fichier ou un répertoire

La commande `rm` permet de supprimer le ou les fichiers spécifiés : `rm [nom_du_fichier]`. Il est possible de supprimer plusieurs fichiers à la fois : `rm [nom_du_fichier1] [nom_du_fichier2] [nom_du_fichier3]`.

#### 4. Créer un répertoire

La commande `mkdir` permet de créer un nouveau répertoire et s'utilise de cette façon : `mkdir [nom_du_répertoire]`.


### III. Affichage

#### 1. Afficher un message

La commande `echo` permet d'afficher un message dans la console : `echo "Hello, world!"`.

#### 2. Afficher le contenu d'un fichier

La commande `cat` permet d'afficher dans la console le contenu d'un fichier spécifié : `cat [nom_du_fichier]`.

#### 3. Afficher les premières lignes d'un fichier

La commande `head` permet d'afficher dans la console les 10 premières lignes d'un fichier spécifié : `head nom_du_fichier`. Il est possible de modifier le nombre de ligne à afficher avec l'option `-n`: `head -n 20 nom_du_fichier`. Dans ce dernier exemple, on affichera les 20 premières lignes du fichier. 

#### 4. Afficher les denières lignes d'un fichier

La commande `tail` permet d'afficher dans la console les 10 denières lignes d'un fichier spécifié : `tail nom_du_fichier`. Il est possible de modifier le nombre de ligne à afficher avec l'option `-n`: `tail -n 20 nom_du_fichier`. Dans ce dernier exemple, on affichera les 20 denières lignes du fichier. 




### IV. Redirections

* `[command] > [fichier]` permet de rediriger la sortie d'une commande vers un fichier.
* `[command] >> [fichier]` permet d'ajouter la sortie d'une commande à la fin d'un fichier.
* `[command1] | [command2]` permet d'utiliser la sortie de command1 comme entrée pour command2.


### V. Documentation

`man [command]` permet d'afficher le manuel d'utilisation de la commande spécifiée. Par exemple, `man echo` donnera toutes les informations nécessaires pour utiliser la commande `echo` à son plein potentiel. C'est une véritable bible et un compagnon de route infaillible. 

Tu verras probablement passer le sigle *RTFM*, qui signifie *Read The Fucking Man*. Si tu as une question, commence toujours par lire le man !
