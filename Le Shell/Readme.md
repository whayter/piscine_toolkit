# Le Shell

Le Shell est un programme d'interprétation de commandes qui tourne dans un terminal. Il offre une interface textuelle permettant à l'utilisateur d'exécuter des commandes pour interagir avec le système d'exploitation, de lancer des programmes ou encore d'automatiser des tâches via des scripts. 


## Pour commencer

Il suffit d'ouvrir un terminal


## Petit glossaire

* **Arborescence** :
* **Chemin** : Relatif / absolu ; On entend par chemin absolu le chemin complet d'un emplacement à partir de la racine du système de fichiers. 
* **Répertoire** : Un répertoire n'est ni plus ni moins qu'un dossier.


## Les principales commandes shell

Les commandes shell sont des instructions textuelles utilisées pour interagir avec le système d'exploitation via un terminal ou une console. Chaque commande est généralement suivie d'options facultatives qui modifient son comportement, et éventuellement d'arguments qui précisent les données sur lesquelles la commande doit agir. Les commandes peuvent effectuer une variété de tâches telles que la navigation dans le système de fichiers, la manipulation de fichiers et de répertoires, le traitement de texte, la gestion des processus, etc. L'utilisation des commandes requiert une connaissance de la syntaxe spécifique à chaque commande ainsi que des options disponibles.

### I. Naviguer dans le système de fichiers

#### 1. Lister les fichiers et dossiers

La commande `ls` (pour *list*) permet de lister les fichiers et dossiers dans le répertoire courant. Voilà quelques options utiles pour cette commande : 
* `-l` permet d'obtenir affichage détaillé (permissions, propriétaire, taille, date de modification)
* `-a` permet d'afficher tous les fichiers, y compris les fichiers cachés (ceux dont le nom commence par un point)
* `-R` permet un affichage récursif des sous-répertoires

#### 2. Naviguer entre les répertoires

La commande `cd`(pour *change directory*) permet de changer de répertoire : `cd [répertoire]`. Il existe quelques raccourcis très pratiques :
* `~` permet d'accéder au répertoire utilisateur (home) : `cd ~`
* `..` permet d'accéder au répertoire parent : `cd ..`
* `-` permet d'accéder au répertoire précédent : `cd -`

#### 3. Afficher le chemin absolu du répertoire courant

La commande `pwd` (pour *print working directory*) permet d'afficher le chemin absolu du répertoire dans lequel on se trouve.

### II. Manipuler les fichiers et répertoires

#### 1. Copier des fichiers ou des répertoires

La commande `cp` (pour *copy*) permet de copier des fichiers ou des répertoires d'un emplacement à un autre : `cp [source] [destination]`.

#### 2. Déplacer ou renommer des fichiers ou des répertoires

La commande `mv` (pour *move*) permet de déplacer des fichiers ou des répertoires d'un emplacement à un autre : `mv [source] [destination]`. Il est aussi possible de déplacer plusieures sources à la fois : `mv [source1] [source2] [destination]`.

Cette commande est également utilisée pour renommer un fichier ou un répertoire : `mv [ancien nom de fichier] [nouveau nom de fichier]`.

#### 3. Supprimer un fichier ou un répertoire

La commande `rm` (pour *remove*) permet de supprimer un fichier spécifié : `rm [fichier]`. Il est également possible de supprimer plusieurs fichiers à la fois : `rm [fichier1] [fichier2] [fichier3]`.

Pour supprimer un répertoire vide, il faut utiliser l'option `-d` (pour *directory*). Sinon, on peut supprimer un répertoire non vide grâce à l'option `-r` (pour *recursive*) : `rm -r [répertoire]`. 

Il convient d'être prudent avec cette commande, les erreurs arrivent vite et peuvent être fatales. L'option `-i` permet d'ajouter une confirmation avant de supprimer chaque fichier spécifié. 

#### 4. Créer un répertoire

La commande `mkdir` (pour *make directory*) permet de créer un nouveau répertoire et s'utilise de cette façon : `mkdir [répertoire]`.

#### 5. Afficher le contenu d'un fichier

La commande `cat` permet d'afficher dans la console le contenu d'un fichier spécifié : `cat [fichier]`. Il est possible d'afficher plusieurs fichiers à la suite en renseignant plusieurs noms de fichiers.

#### 6. Afficher les premières lignes d'un fichier

La commande `head` permet d'afficher dans la console les 10 premières lignes d'un fichier spécifié : `head [fichier]`. Il est possible de modifier le nombre de lignes à afficher avec l'option `-n`: `head -n 20 [fichier]`. Dans ce dernier exemple, on affichera les 20 premières lignes du fichier. 

#### 7. Afficher les denières lignes d'un fichier

La commande `tail` permet d'afficher dans la console les 10 denières lignes d'un fichier spécifié : `tail [fichier]`. Il est possible de modifier le nombre de lignes à afficher avec l'option `-n`: `tail -n 20 [fichier]`. Dans ce dernier exemple, on affichera les 20 denières lignes du fichier. 







QUELLE CAT2GORIE ?
#### 5. Afficher un message
La commande `echo` permet d'afficher un message dans la console : `echo "Hello, world!"`.



commandes à traiter : 

grep
find
sed
env
export



### III. Redirections

Le shell exprime toute sa puissance grâce à la redirection. Il est possible de rediriger la sortie d'une commande vers l'entrée d'une autre commande, ou vers un fichier, et de chaîne ainsi différentes commmandes pour éxecuter une tâche complexe. 

#### 1. Rediriger la sortie d'une commande vers un fichier

Le symbole `>` permet de rediriger la sortie d'une commande vers un fichier : `[command] > [fichier]`. Par exemple, `echo "Hello, World!" > hello.txt` va éxecuter la commande `echo` puis écrire le résultat dans le fichier `hello.txt`. À noter : si le fichier n'existe pas, il sera créé par cette commande.

#### 2. Ajouter la sortie d'une commande à la fin d'un fichier

Le symbole `>>` permet d'ajouter la sortie d'une commande à la fin d'un fichier : `[command] >> [fichier]`. Par exemple, `echo "Hello, World!" >> hello.txt` va éxecuter la commande `echo` puis écrire le résultat à la fin du fichier `hello.txt`. À noter : si le fichier n'existe pas, il sera créé par cette commande.

#### 3. Utiliser le contenu d'un fichier comme entrée pour une commande

Le symbole `<`permet d'utiliser le contenu d'un fichier commme entrée pour une commande : `[command] < [fichier]`. Par exemple, `wc -l < file.txt`

#### 4. Rediriger la sortie d'une commande vers l'entrée d'une autre commande

Il est possible de chaîner des commandes grâce au symbole `|` (appelé *pipe*), permettant ainsi d'utiliser la sortie d'une commande comme entrée d'une autre commande : `[command1] | [command2]`. 

Pour prendre un exemple concret, 


### V. Documentation

`man [command]` permet d'afficher le manuel d'utilisation de la commande spécifiée. Par exemple, `man echo` donnera toutes les informations nécessaires pour utiliser la commande `echo` à son plein potentiel. C'est une véritable bible et un compagnon de route infaillible. 

Tu verras probablement passer le sigle *RTFM*, qui signifie *Read The Fucking Man*. Si tu as une question, commence toujours par lire le manuel !


## Les scripts shell

Un script shell est un fichier contennant des commandes et ayant pour extension `.sh`. 

Il existe différents programmes shell. Sur la première ligne d'un script, on déclare quel programme shell doit être utilisé pour l'exécution. Par défaut, c'est *Bash* qui est utilisé. La déclaration prend alors cette forme : `#!/bin/bash`. 

Une fois le script créé, il faut modifier les droits pour le rendre exécutable : `chmod +x mon_script.sh`.

On exécute ensuite le script de cette façon : `./mon_script.sh`. Si le script attend des paramètres, `./mon_script.sh [paramètre1] [paramètre2]`

Les commentaires dans un script shell sont préfixé du symbole `#`

