# Git

Git est un outil qui permet de garder une trace des différentes versions d'un projet informatique. Ainsi toutes les modifications apportées dans un projet sont enregistrées et il est donc possible de revenir en arrière si nécessaire. Dans le cadre d'un travail collaboratif, Git permet à chacun de voir ce que les autres ont fait et de combiner leurs changements de manière ordonnée.


## Les principales commandes

### Créer un dépôt

Pour commencer à travailler avec Git, deux options s'offrent à nous :

#### 1. Cloner un dépôt distant :
Il est possible de créer une copie locale d'un dépôt distant grâce à la commande `git clone [url]`, où `[url]` est l'adresse du dépôt que l'on souhaite récupérer.

#### 2. Initier un nouveau dépôt :
On peut également initier un nouveau dépôt dans le répertoire courant avec la commande `git init`. Dans ce cas, il faudra également associer ce dépôt local à un dépôt distant en utilisant la commande `git remote add origin [url]`, où `[url]` est l'adresse du dépôt distant que l'on souhaite associer.

Créer des versions

On peut maintenant commencer à travailler sur notre projet. 


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
