# Git

Git est un outil qui permet de garder une trace des différentes versions d'un projet informatique. Ainsi toutes les modifications apportées dans un projet sont enregistrées et il est donc possible de revenir en arrière si nécessaire. Dans le cadre d'un travail collaboratif, Git permet à chacun de voir ce que les autres ont fait et de combiner leurs changements de manière ordonnée.


## Créer un dépôt Git

Pour commencer à travailler avec Git, deux options s'offrent à nous :

### 1. Cloner un dépôt distant :
Il est possible de créer une copie locale d'un dépôt distant grâce à la commande `git clone [url]`, où `[url]` est l'adresse du dépôt que l'on souhaite récupérer.

### 2. Initier un nouveau dépôt :
On peut également initier un nouveau dépôt dans le répertoire courant avec la commande `git init`. Dans ce cas, il faudra également associer ce dépôt local à un dépôt distant en utilisant la commande `git remote add origin [url]`, où `[url]` est l'adresse du dépôt distant que l'on souhaite associer.


## Gérer les modifications avec Git

Après avoir créé ou cloné un dépôt, voici les commandes essentielles pour gérer les modifications et suivre l'évolution de son projet :

### 1. Ajouter des fichiers à la zone de staging :

On utilise la commande `git add` pour ajouter un fichier modifié à la **zone de staging**. Il est possible d'ajouter plusieurs fichiers à la fois, et même d'ajouter tous les fichiers modifiés : 
```bash
git add fichier            # ajout d'un fichier spécifique
git add fichier1 fichier2  # ajout de deux fichiers spécifiques
git add .                  # ajout de l'ensemble des fichiers modifiés
```

### 2. Faire un commit :
La commande `git commit` enregistre les modifications de la zone de staging dans l'historique du dépôt. Chaque commit doit être accompagné d'un message décrivant les changements. elle s'utilise de cette façon : 
```bash
git commit -m "Description des modifications"
```

sh
Copier le code
git commit -m "Description des modifications"
Vérifier l'état des fichiers :
La commande git status affiche l'état actuel du répertoire de travail et de la zone de staging. Elle indique les fichiers modifiés, ajoutés, ou supprimés, ainsi que ceux qui sont prêts à être committés.

sh
Copier le code
git status
Consulter l'historique des commits :
Utilisez la commande git log pour afficher l'historique des commits du dépôt. Cette commande montre les messages de commit, les auteurs, et les dates des changements.

sh
Copier le code
git log
Pousser les modifications vers le dépôt distant :
Une fois les modifications committées, vous pouvez les envoyer vers le dépôt distant avec la commande git push. Cette commande synchronise votre dépôt local avec le dépôt distant, permettant ainsi à d'autres collaborateurs de voir vos changements.

sh














Une fois qu'on a un dépôt local, on peut commencer à travailler. Les commandes suivantes permettent d'enregistrer les modifications apportées sur le dépôt local vers le dépôt distant :
* `git status` permet de voir l'état actuel de notre dépôt local. On voit ainsi quels fichiers ont été modifiés, ajoutés ou supprimés du projet. 
* `git add [fichier]` : cette commande indique à git quels fichiers doivent être inclus dans le prochain commit. Lorsqu'on ajoute un fichier avec cette commande, celui-ci se retrouve dans une zone dite de staging.
* `git commit -m [message]` : permet d'enregistrer les modifications apportées en créant un snapshot. Il est important de renseigner un message explicite pour s'y retrouver plus facilement entre les commits
* `git push` : permet d'envoyer les modifications commitées vers le dépôt distant


* `git status`

  
* `git log` : sert à afficher l'historique des commmits
* `git diff [hash1] [hash2]` : permet d'afficher les différences entre deux versions
* `git fetch`
* `git pull`
* `git branch`
* `git checkout`
* `git merge`
